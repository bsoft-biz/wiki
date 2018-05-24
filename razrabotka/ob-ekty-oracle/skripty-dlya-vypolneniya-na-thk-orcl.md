# Скрипты для выполнения на THK@ORCL

```sql
alter table tmdb_sld_tvr_realiz_m add (
 constraint tmdb_sld_tvr_realiz_m_fk
foreign key (nrdoc)
references tmdb_docs (cod)
 on delete cascade deferrable initially deferred);
```

```sql
alter table tmdb_sld_tvr_realiz_d add (
 constraint tmdb_sld_tvr_realiz_d_fk
foreign key (nrdoc)
references tmdb_docs (cod)
 on delete cascade deferrable initially deferred);
```

```sql
alter table tmdb_trade_m add (
 constraint tmdb_trade_m_fk
 foreign key (nrdoc)
 references tmdb_docs (cod)
 on delete cascade
 deferrable initially deferred);
```

```sql
alter table tmdb_trade_d add (
 constraint tmdb_trade_d_fk
 foreign key (nrdoc)
 references tmdb_docs (cod)
 on delete cascade
 deferrable initially deferred);
```



