## 建立資料表的語法

'''sql語法程式區塊
CREATE TABLE [IF NOT EXISTS] table_name (
   column1 datatype(length) column_constraint,
   column2 datatype(length) column_constraint,
   ...
   table_constraints
);
## 建立一個sudent的資料表
'''sql
CREATE TABLE IF NOT EXIST student(
    student_id SERIAL PRIMARY KEY,
    name VARCHAR(20) NOT NULL,
    major VARCHAR(20) UNIQUE
);
'''