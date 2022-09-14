# dbms-exp3
Enter password: *******

Welcome to the MySQL monitor.  Commands end with ; or \g.

Your MySQL connection id is 9

Server version: 8.0.30 MySQL Community Server - GPL

 

Copyright (c) 2000, 2022, Oracle and/or its affiliates.

 

Oracle is a registered trademark of Oracle Corporation and/or its

affiliates. Other names may be trademarks of their respective

owners.

 

Type 'help;' or '\h' for help. Type '\c' to clear the current input statement.

 

mysql> use db;

Database changed

mysql> create table dept(DeptNo int(3),DeptName varchar(20),deptloc varchar(20));

ERROR 1050 (42S01): Table 'dept' already exists

mysql> drop table dept;

Query OK, 0 rows affected (0.01 sec)

 

mysql> create table dept(DeptNo int(3),DeptName varchar(20),deptloc varchar(20));

Query OK, 0 rows affected, 1 warning (0.01 sec)

 

mysql> desc dept;

+----------+-------------+------+-----+---------+-------+

| Field    | Type        | Null | Key | Default | Extra |

+----------+-------------+------+-----+---------+-------+

| DeptNo   | int         | YES  |     | NULL    |       |

| DeptName | varchar(20) | YES  |     | NULL    |       |

| deptloc  | varchar(20) | YES  |     | NULL    |       |

+----------+-------------+------+-----+---------+-------+

3 rows in set (0.00 sec)

 

mysql> insert into table dept values(203,'IT',)

    ->

    -> insert into table dept values(203,'IT','Madurai');

ERROR 1064 (42000): You have an error in your SQL syntax; check the manual that corresponds to your MySQL server version for the right syntax to use near 'table dept values(203,'IT',)

 

insert into table dept values(203,'IT','Madurai')' at line 1

mysql> insert into table dept values(203,'IT','Madurai');

ERROR 1064 (42000): You have an error in your SQL syntax; check the manual that corresponds to your MySQL server version for the right syntax to use near 'table dept values(203,'IT','Madurai')' at line 1

mysql> insert into dept values(203,'IT','Madurai');

Query OK, 1 row affected (0.01 sec)

 

mysql> create table Emp(empno int(3), ename varchar(20),Job char(15),deptno int(3),sal int(7));

ERROR 1050 (42S01): Table 'emp' already exists

mysql> drop table emp;

Query OK, 0 rows affected (0.01 sec)

 

mysql> create table Emp(empno int(3), ename varchar(20),Job char(15),deptno int(3),sal int(7));

Query OK, 0 rows affected, 3 warnings (0.01 sec)

 

mysql> desc emp;

+--------+-------------+------+-----+---------+-------+

| Field  | Type        | Null | Key | Default | Extra |

+--------+-------------+------+-----+---------+-------+

| empno  | int         | YES  |     | NULL    |       |

| ename  | varchar(20) | YES  |     | NULL    |       |

| Job    | char(15)    | YES  |     | NULL    |       |

| deptno | int         | YES  |     | NULL    |       |

| sal    | int         | YES  |     | NULL    |       |

+--------+-------------+------+-----+---------+-------+

5 rows in set (0.00 sec)

 

mysql> insert into emp values((123,'Ram','Software Developer',232,200000),(145,'Seetha','App Designer',437,150000));

ERROR 1136 (21S01): Column count doesn't match value count at row 1

mysql> insert into emp values(123,'Ram','Software Developer',232,200000),(145,'Seetha','App Designer',437,150000);

ERROR 1406 (22001): Data too long for column 'Job' at row 1

mysql> insert into emp values(123,'Ram','App Developer',232,200000),(145,'Seetha','App Designer',437,150000);

Query OK, 2 rows affected (0.00 sec)

Records: 2  Duplicates: 0  Warnings: 0

 

mysql> select * from emp;

+-------+--------+---------------+--------+--------+

| empno | ename  | Job           | deptno | sal    |

+-------+--------+---------------+--------+--------+

|   123 | Ram    | App Developer |    232 | 200000 |

|   145 | Seetha | App Designer  |    437 | 150000 |

+-------+--------+---------------+--------+--------+

2 rows in set (0.00 sec)

 

mysql> update emp set sal=15000 where Job='App developer';

Query OK, 1 row affected (0.00 sec)

Rows matched: 1  Changed: 1  Warnings: 0

 

mysql> select * from emp;

+-------+--------+---------------+--------+--------+

| empno | ename  | Job           | deptno | sal    |

+-------+--------+---------------+--------+--------+

|   123 | Ram    | App Developer |    232 |  15000 |

|   145 | Seetha | App Designer  |    437 | 150000 |

+-------+--------+---------------+--------+--------+

2 rows in set (0.00 sec)

 

mysql> create table employee(empno int(3), ename varchar(20),Job char(15),deptno int(3),sal int(7));

Query OK, 0 rows affected, 3 warnings (0.01 sec)

 

mysql> insert into emp values(23,'Ram','HR-manager',23,20000),(14,'Seetha','manager',47,15000);

Query OK, 2 rows affected (0.00 sec)

Records: 2  Duplicates: 0  Warnings: 0

 

mysql> insert into employee values(23,'Ram','HR-manager',23,20000),(14,'Seetha','manager',47,15000);

Query OK, 2 rows affected (0.00 sec)

Records: 2  Duplicates: 0  Warnings: 0

 

mysql> select * from employee;

+-------+--------+------------+--------+-------+

| empno | ename  | Job        | deptno | sal   |

+-------+--------+------------+--------+-------+

|    23 | Ram    | HR-manager |     23 | 20000 |

|    14 | Seetha | manager    |     47 | 15000 |

+-------+--------+------------+--------+-------+

2 rows in set (0.00 sec)

 

mysql> select ename, Job from emp;

+--------+---------------+

| ename  | Job           |

+--------+---------------+

| Ram    | App Developer |

| Seetha | App Designer  |

| Ram    | HR-manager    |

| Seetha | manager       |

+--------+---------------+

4 rows in set (0.00 sec)

 

mysql> create table Emp2(empno int(3), ename varchar(20),Job char(15),deptno int(3),sal int(7));

Query OK, 0 rows affected, 3 warnings (0.01 sec)

 

mysql> create table Employee2(empno int(3), ename varchar(20),Job char(15),deptno int(3),sal int(7));

Query OK, 0 rows affected, 3 warnings (0.01 sec)

 

mysql> insert into employee values(23,'Ram','HR-manager',23,20000),(14,'Seetha','manager',47,15000);

Query OK, 2 rows affected (0.01 sec)

Records: 2  Duplicates: 0  Warnings: 0

 

mysql> insert into Employee2 values(23,'Ram','HR-manager',23,20000),(14,'Seetha','manager',47,15000);

Query OK, 2 rows affected (0.01 sec)

Records: 2  Duplicates: 0  Warnings: 0

 

mysql> INSERT into emp2 values(select * from Employee2);

ERROR 1064 (42000): You have an error in your SQL syntax; check the manual that corresponds to your MySQL server version for the right syntax to use near 'select * from Employee2)' at line 1

mysql> INSERT into emp2 (empno,ename,Job,deptno,sal) select empno,ename,Job,deptno,sal from Employee2;

Query OK, 2 rows affected (0.01 sec)

Records: 2  Duplicates: 0  Warnings: 0

 

mysql> select * from emp2;

+-------+--------+------------+--------+-------+

| empno | ename  | Job        | deptno | sal   |

+-------+--------+------------+--------+-------+

|    23 | Ram    | HR-manager |     23 | 20000 |

|    14 | Seetha | manager    |     47 | 15000 |

+-------+--------+------------+--------+-------+

2 rows in set (0.00 sec)

 

mysql> delete * from emp2 where JOB='HR-manager';

ERROR 1064 (42000): You have an error in your SQL syntax; check the manual that corresponds to your MySQL server version for the right syntax to use near '* from emp2 where JOB='HR-manager'' at line 1

mysql> delete from emp2 where JOB='HR-manager';

Query OK, 1 row affected (0.00 sec)

 

mysql> select * from emp2;

+-------+--------+---------+--------+-------+

| empno | ename  | Job     | deptno | sal   |

+-------+--------+---------+--------+-------+

|    14 | Seetha | manager |     47 | 15000 |

+-------+--------+---------+--------+-------+

1 row in set (0.00 sec)

 

mysql> select * from Employee2 whwere deptno=47;

ERROR 1064 (42000): You have an error in your SQL syntax; check the manual that corresponds to your MySQL server version for the right syntax to use near 'deptno=47' at line 1

mysql> select * from Employee2 whwere deptno==47;

ERROR 1064 (42000): You have an error in your SQL syntax; check the manual that corresponds to your MySQL server version for the right syntax to use near 'deptno==47' at line 1

mysql> select * from Employee2 where deptno=47;

+-------+--------+---------+--------+-------+

| empno | ename  | Job     | deptno | sal   |

+-------+--------+---------+--------+-------+

|    14 | Seetha | manager |     47 | 15000 |

+-------+--------+---------+--------+-------+

1 row in set (0.00 sec)

 

mysql> select deptno from Employee2 order by deptno as duplicatecount;

ERROR 1064 (42000): You have an error in your SQL syntax; check the manual that corresponds to your MySQL server version for the right syntax to use near 'as duplicatecount' at line 1

mysql> select deptno from Employee2 order by deptno as DuplicateCount;

ERROR 1064 (42000): You have an error in your SQL syntax; check the manual that corresponds to your MySQL server version for the right syntax to use near 'as DuplicateCount' at line 1

mysql> select deptno from Employee2 order by deptno;

+--------+

| deptno |

+--------+

|     23 |

|     47 |

+--------+

2 rows in set (0.00 sec)

 

mysql> select * from employee2;

+-------+--------+------------+--------+-------+

| empno | ename  | Job        | deptno | sal   |

+-------+--------+------------+--------+-------+

|    23 | Ram    | HR-manager |     23 | 20000 |

|    14 | Seetha | manager    |     47 | 15000 |

+-------+--------+------------+--------+-------+

2 rows in set (0.00 sec)

 

mysql> insert into Employee2 values(23,'Ram','HR-manager',23,20000),(14,'Seetha','manager1',47,15000);

Query OK, 2 rows affected (0.00 sec)

Records: 2  Duplicates: 0  Warnings: 0

 

mysql> select * from employee2;

+-------+--------+------------+--------+-------+

| empno | ename  | Job        | deptno | sal   |

+-------+--------+------------+--------+-------+

|    23 | Ram    | HR-manager |     23 | 20000 |

|    14 | Seetha | manager    |     47 | 15000 |

|    23 | Ram    | HR-manager |     23 | 20000 |

|    14 | Seetha | manager1   |     47 | 15000 |

+-------+--------+------------+--------+-------+

4 rows in set (0.00 sec)

 

mysql> select distinct deptno from employee2;

+--------+

| deptno |

+--------+

|     23 |

|     47 |

+--------+

2 rows in set (0.00 sec)

 

mysql> select distinct deptno,empno from employee2;

+--------+-------+

| deptno | empno |

+--------+-------+

|     23 |    23 |

|     47 |    14 |

+--------+-------+

2 rows in set (0.00 sec)

