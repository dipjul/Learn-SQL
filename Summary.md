# Learn SQL
1. Show the databases already available
```mysql
show databases;
```
2. Create a database names mydatabase
```mysql
create database mydatabase;
```
3. Go inside/ to select the database named mydatabase
```mysql
use mydatabase;
```
4. To view which database are you using currently
```mysql
select database();
```
5. To delete a database named mydatabase
```mysql
drop database mydatabase
```
6. To create a table named demo with columns id(int) and name(string of length 50)
```mysql
create table demo (
  id int,
  name varchar(50)
);
```
7. To show all the tables present in a database
```mysql
show tables;
```
8. To see the table structure of table named demo
```mysql
describe demo;
desc demo;
```
9. To delete a table named demo
```mysql
drop table demo;
```
10. Insert data into the table demo
```mysql
 INSERT INTO demo (id, name) VALUES (1,"pop");
 INSERT INTO demo VALUES (2,"push");
```
11. To view the data in a table
```mysql
select * from demo;
```
12. Insert the name hel'la into the table
```mysql
INSERT INTO demo (id, name) values (3,"Hel'la");
INSERT INTO demo (id, name) values (3,'Hel\'la');
```
13. Insert more than 1 record at once
```mysql
INSERT INTO demo (id, name) values (5,'la'), (6,'Hea');
```
14. Create a table with few colums that can't be null
```mysql
CREATE TABLE employee (
  firstname VARCHAR(20) NOT NULL,
  middlename VARCHAR(20),
  lastname VARCHAR(20) NOT NULL,
  age INT NOT NULL,
  salary INT NOT NULL,
  location VARCHAR(20) NOT NULL);
```
15. How to have default values for a column in a table?
```mysql
CREATE TABLE employee (
  firstname VARCHAR(20) NOT NULL,
  middlename VARCHAR(20),
  lastname VARCHAR(20) NOT NULL,
  age INT NOT NULL,
  salary INT NOT NULL,
  location VARCHAR(20) DEFAULT 'hyderabad');
```
16. Insert only the not nullable column's data
```mysql
INSERT INTO employee (
  firstname, lastname, age, salary) values('G\'la', 'Vani', 27, 100000);
```
17. On the employee table can we set the location(default) as null?
```mysql
-- yes we can
INSERT INTO employee (
  firstname, lastname, age, salary, location) values('T\'ia', 'Hani', 24, 105000, null);
```
18. How to have default values for a column (not nullable) in a table?
```mysql
CREATE TABLE employee (
  firstname VARCHAR(20) NOT NULL,
  middlename VARCHAR(20),
  lastname VARCHAR(20) NOT NULL,
  age INT NOT NULL,
  salary INT NOT NULL,
  location VARCHAR(20) NOT NULL DEFAULT 'hyderabad');
```
