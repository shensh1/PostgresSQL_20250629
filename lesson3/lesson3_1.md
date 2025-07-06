## 建立資料表的語法

```sql語法程式區塊
CREATE TABLE [IF NOT EXISTS] table_name (
   column1 datatype(length) column_constraint,
   column2 datatype(length) column_constraint,
   ...
   table_constraints
);
```sql

## 建立一個sudent的資料表
```sql
CREATE TABLE IF NOT EXISTS student(
    student_id SERIAL PRIMARY KEY,
    name VARCHAR(20) NOT NULL,
    major VARCHAR(20) UNIQUE
);
```sql

## 刪除資料表
```sql
DROP TABEL IF EXISTS student;
```sql

## 新增1筆資料表
```sql
INSERT INTO student (name, major)
VALUES ('沈淑淮', '歷史');
```sql

## 新增多筆資料表
```sql
INSERT INTO student (name, major) 
VALUES  ('小柱','生物'),
        ('小淮','英文');
```sql

