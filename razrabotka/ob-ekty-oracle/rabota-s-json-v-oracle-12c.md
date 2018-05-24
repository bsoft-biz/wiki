# Работа с JSON в Oracle 12c

**Источник:**

[https://docs.oracle.com/database/121/ADXDB/json.htm\#ADXDB6247](https://docs.oracle.com/database/121/ADXDB/json.htm#ADXDB6247)

**Примеры работают в Oracle начиная с версии 12**

```sql
-- Таблица с проверкой на валидность JSON
CREATE TABLE j_purchaseorder
   (id          RAW (16) NOT NULL,
    date_loaded TIMESTAMP WITH TIME ZONE,
    po_document CLOB
    CONSTRAINT ensure_json CHECK (po_document IS JSON));
-- Данные, содержащие массив
INSERT INTO j_purchaseorder
  VALUES (1,
          SYSTIMESTAMP,
          '{ "PONumber"             : 1600,
  "Reference"            : "ABULL-20140421",
  "Requestor"            : "Alexis Bull",
  "User"                 : "ABULL",
  "CostCenter"           : "A50",
  "ShippingInstructions" : { "name"   : "Alexis Bull",
                             "Address": { "street"  : "200 Sporting Green",
                                          "city"    : "South San Francisco",
                                          "state"   : "CA",
                                          "zipCode" : 99236,
                                          "country" : "United States of America" },
                             "Phone" : [ { "type" : "Office", "number" : "909-555-7307" },
                                         { "type" : "Mobile", "number" : "415-555-1234" } ] },
  "Special Instructions" : null,
  "AllowPartialShipment" : false,
  "LineItems"            : [ { "ItemNumber" : 1,
                               "Part"       : { "Description" : "One Magic Christmas",
                                                "UnitPrice"   : 19.95,
                                                "UPCCode"     : 13131092899 },
                               "Quantity"   : 9.0 },
                             { "ItemNumber" : 2,
                               "Part"       : { "Description" : "Lethal Weapon",
                                                "UnitPrice"   : 19.95,
                                                "UPCCode"     : 85391628927 },
                               "Quantity"   : 5.0 } ] }');
 
SELECT select_list
  FROM --table,
       json_table(column, '$' error_handler ON ERROR
         COLUMNS ("COLUMN_ALIAS" NUMBER EXISTS PATH json_path)) AS "JT"
  WHERE jt.column_alias = 1;

SELECT jt.requestor, jt.phones
  FROM j_purchaseorder,
       json_table(po_document, '$'
         COLUMNS (requestor VARCHAR2(32 CHAR) PATH '$.Requestor',
                  phones    VARCHAR2(100 CHAR) FORMAT JSON
                            PATH '$.ShippingInstructions.Phone',
                  partial   NUMBER(1) PATH '$.AllowPartialShipment',
                  has_zip   VARCHAR2(5 CHAR) EXISTS
                            PATH '$.ShippingInstructions.Address.zipCode')) jt
  WHERE jt.partial = 0 AND has_zip = 'true';
 
SELECT jt.*
  FROM j_purchaseorder,
       json_table(po_document, '$'
         COLUMNS (requestor VARCHAR2(32 CHAR) PATH '$.Requestor',
                  ph_arr    VARCHAR2(100 CHAR) FORMAT JSON
                            PATH '$.ShippingInstructions.Phone')) AS "JT";
           

-- Выборка из массива телефонов
SELECT jt.*
  FROM j_purchaseorder,
       json_table(po_document, '$.ShippingInstructions.Phone[*]'
         COLUMNS (phone_type VARCHAR2(10) PATH '$.type',
                  phone_num  VARCHAR2(20) PATH '$.number')) AS "JT";
               

-- Выборка из массива LineItems
SELECT jt.*
  FROM j_purchaseorder,
       json_table(po_document, '$.LineItems[*]'
         COLUMNS (ItemNumber VARCHAR2(10) PATH '$.ItemNumber',
                  Description  VARCHAR2(20) PATH '$.Part.Description')) AS "JT";

SELECT jt.*
  FROM j_purchaseorder,
       json_table(po_document, '$'
         COLUMNS (
           requestor  VARCHAR2(32 CHAR) PATH '$.Requestor',
           phone_type VARCHAR2(50 CHAR) FORMAT JSON WITH WRAPPER
                      PATH '$.ShippingInstructions.Phone[*].type',
           phone_num  VARCHAR2(50 CHAR) FORMAT JSON WITH WRAPPER
                      PATH '$.ShippingInstructions.Phone[*].number')) AS "JT";                  

-- Выборка с объединением основных столбцов и столбцов массива (перемножаются)
SELECT jt.*
  FROM j_purchaseorder,
       json_table(po_document, '$'
         COLUMNS (
           requestor VARCHAR2(32 CHAR) PATH '$.Requestor',
           NESTED                      PATH '$.ShippingInstructions.Phone[*]'
             COLUMNS (phone_type VARCHAR2(32 CHAR) PATH '$.type',
                      phone_num  VARCHAR2(20 CHAR) PATH '$.number'))) AS "JT";

-- Выборка с объединением всех основных столбцов и столбцов массива (перемножаются)
CREATE OR REPLACE VIEW j_purchaseorder_detail_view AS
  SELECT d.*
    FROM j_purchaseorder po,
         json_table(po.po_document, '$'
           COLUMNS (
             po_number        NUMBER(10)         PATH '$.PONumber',
             reference        VARCHAR2(30 CHAR)  PATH '$.Reference',
             requestor        VARCHAR2(128 CHAR) PATH '$.Requestor',
             userid           VARCHAR2(10 CHAR)  PATH '$.User',
             costcenter       VARCHAR2(16)       PATH '$.CostCenter',
             ship_to_name     VARCHAR2(20 CHAR)
                              PATH '$.ShippingInstructions.name',
             ship_to_street   VARCHAR2(32 CHAR)
                              PATH '$.ShippingInstructions.Address.street',
             ship_to_city     VARCHAR2(32 CHAR)
                              PATH '$.ShippingInstructions.Address.city',
             ship_to_county   VARCHAR2(32 CHAR)
                              PATH '$.ShippingInstructions.Address.county',
             ship_to_postcode VARCHAR2(10 CHAR)
                              PATH '$.ShippingInstructions.Address.postcode',
             ship_to_state    VARCHAR2(2 CHAR)
                              PATH '$.ShippingInstructions.Address.state',
             ship_to_zip      VARCHAR2(8 CHAR)
                              PATH '$.ShippingInstructions.Address.zipCode',
             ship_to_country  VARCHAR2(32 CHAR)
                              PATH '$.ShippingInstructions.Address.country',
             ship_to_phone    VARCHAR2(24 CHAR)
                              PATH '$.ShippingInstructions.Phone[0].number',
             NESTED PATH '$.LineItems[*]'
               COLUMNS (
                 itemno      NUMBER(38)         PATH '$.ItemNumber', 
                 description VARCHAR2(256 CHAR) PATH '$.Part.Description', 
                 upc_code    VARCHAR2(14 CHAR)  PATH '$.Part.UPCCode', 
                 quantity    NUMBER(12,4)       PATH '$.Quantity', 
                 unitprice   NUMBER(14,2)       PATH '$.Part.UnitPrice'))) d;
             
-- Выборка с фильтром по значению поля json
SELECT jt.*
  FROM j_purchaseorder po,
       json_table(po.po_document, '$'
         COLUMNS po_number  NUMBER(5) PATH '$.PONumber',
                 reference  VARCHAR2(30 CHAR) PATH '$.Reference',
                 requestor  VARCHAR2(32 CHAR) PATH '$.Requestor',
                 userid     VARCHAR2(10 CHAR) PATH '$.User',
                 costcenter VARCHAR2(16 CHAR) PATH '$.CostCenter') jt
  WHERE po_number = 1600;
  -- Выборка с объединением основных столбцов, столбцов массива и столбцов массива телефонов (перемножаются)
 SELECT d.*
    FROM j_purchaseorder po,
         json_table(po.po_document, '$'
           COLUMNS (
             po_number        NUMBER(10)         PATH '$.PONumber',
             reference        VARCHAR2(30 CHAR)  PATH '$.Reference',
             requestor        VARCHAR2(128 CHAR) PATH '$.Requestor',
             userid           VARCHAR2(10 CHAR)  PATH '$.User',
             costcenter       VARCHAR2(16)       PATH '$.CostCenter',
             ship_to_name     VARCHAR2(20 CHAR)
                              PATH '$.ShippingInstructions.name',
             ship_to_street   VARCHAR2(32 CHAR)
                              PATH '$.ShippingInstructions.Address.street',
             ship_to_city     VARCHAR2(32 CHAR)
                              PATH '$.ShippingInstructions.Address.city',
             ship_to_county   VARCHAR2(32 CHAR)
                              PATH '$.ShippingInstructions.Address.county',
             ship_to_postcode VARCHAR2(10 CHAR)
                              PATH '$.ShippingInstructions.Address.postcode',
             ship_to_state    VARCHAR2(2 CHAR)
                              PATH '$.ShippingInstructions.Address.state',
             ship_to_zip      VARCHAR2(8 CHAR)
                              PATH '$.ShippingInstructions.Address.zipCode',
             ship_to_country  VARCHAR2(32 CHAR)
                              PATH '$.ShippingInstructions.Address.country',
             ship_to_phone    VARCHAR2(24 CHAR)
                              PATH '$.ShippingInstructions.Phone[0].number',
             NESTED PATH '$.LineItems[*]'
               COLUMNS (
                 itemno      NUMBER(38)         PATH '$.ItemNumber', 
                 description VARCHAR2(256 CHAR) PATH '$.Part.Description', 
                 upc_code    VARCHAR2(14 CHAR)  PATH '$.Part.UPCCode', 
                 quantity    NUMBER(12,4)       PATH '$.Quantity', 
                 unitprice   NUMBER(14,2)       PATH '$.Part.UnitPrice'),
           NESTED PATH '$.ShippingInstructions.Phone[*]'
               COLUMNS (
                 type1   VARCHAR2(256 CHAR)        PATH '$.type', 
                 number1 VARCHAR2(256 CHAR) PATH '$.number')                 
                 )) d
```

