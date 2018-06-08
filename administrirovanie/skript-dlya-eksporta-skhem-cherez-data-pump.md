# Скрипт для экспорта схем через data pump

 Скрипт нужно положить в папку dpump  
и указать правильные пути

```bash
vim /mnt/sys1000/oracle/admin/orcl/dpdump/exdp
```

```bash
#!/bin/bash
# oracle: DUMP
# chkconfig: 345
# processname: dump

. /etc/rc.d/init.d/functions

ORACLE_HOME=/mnt/sys1000/oracle/product/11.2.0.4/db_1
ORACLE_BASE_ADMIN=/mnt/sys1000/oracle/admin
ORACLE_USER=oracle
ORACLE_SID=orcl
ORACLE_SHEMAS=(SHEMAS1 SHEMAS2 SHEMAS3 SHEMAS4)
#EXP_DIR=/var/un4/exdp


for (( i=0; i<${#ORACLE_SHEMAS[@]}; i++ ));
do

dp=`date "+%d%m%y_%H-%M"`

echo -n $"Starting Oracle Dump ${ORACLE_SHEMAS[$i]}"
echo \

su - $ORACLE_USER -c  "$ORACLE_HOME/bin/expdp \'sys/sys@$ORACLE_SID as sysdba\' directory=data_pump_dir schemas=${ORACLE_SHEMAS[$i]} dumpfile=${ORACLE_SHEMAS[$i]}-$dp.dmp  logfile=${ORACLE_SHEMAS[$i]}-$dp.log"

cd $ORACLE_BASE_ADMIN/$ORACLE_SID/dpdump

#tar -czf $EXP_DIR/${ORACLE_SHEMAS[$i]}-$dp.tar.gz ${ORACLE_SHEMAS[$i]}-$dp.dmp ${ORACLE_SHEMAS[$i]}-$dp.log

tar -czf ${ORACLE_SHEMAS[$i]}-$dp.tar.gz ${ORACLE_SHEMAS[$i]}-$dp.dmp ${ORACLE_SHEMAS[$i]}-$dp.log

smbclient //IP/Share  password -U user -c "put ${ORACLE_SHEMAS[$i]}-$dp.tar.gz; exit"

su - $ORACLE_USER -c  "$ORACLE_HOME/bin/sqlplus -s sys/sys@$ORACLE_SID as sysdba  <<EOF
insert into UN4PUBLIC.UN4DPLOG (dt, schema, filename) values (sysdate,'${ORACLE_SHEMAS[$i]}', '${ORACLE_SHEMAS[$i]}-$dp.tar.gz');
EOF
"
rm -f ${ORACLE_SHEMAS[$i]}-$dp.dmp ${ORACLE_SHEMAS[$i]}-$dp.log ${ORACLE_SHEMAS[$i]}-$dp.tar.gz

done
```

 Назначить запуск в кроне

```bash
crontab -u root -e
```

 пример

```bash
30 17 * * * /mnt/sys1000/oracle/admin/orcl/dpdump/exdp
```



