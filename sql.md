# SQL

#### Move Tables

To move tables from one tablespace to another:

```sql  SELECT ‘ALTER TABLE ‘ || table_name || ‘ MOVE TABLESPACE TABLE_SPACE_2;’ FROM user_tables WHERE tablespace_name != TABLE_SPACE_2 ORDER BY 1; ```

The above query produces a number of SQL statements that can then be executed in SQL Developer

