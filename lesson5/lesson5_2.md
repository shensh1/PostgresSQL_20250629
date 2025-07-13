
--DROP TABLE IF EXISTS employee CASCADE; CASCADE與有關連的表格也一併刪除
DROP TABLE IF EXISTS employee;

CREATE TABLE employee(
	emp_id SERIAL,
	name VARCHAR(20),
	birth_date DATE,
	sex VARCHAR(20),
	salary INT,
	branch_id INT,
	sup_id INT,
	PRIMARY KEY(emp_id)
);
```