## DS lecture 
1. What is file ?
	- A file is a collection of records , where a record consists of one or more fields .
	- Each record contains same sequence of file.
	- Each field is normally of fixed length.
	- A sample file with four records is shown below.

| Roll no | Name  | Year | Marks |
| ------- | ----- | ---- | ----- |
| 2       | Mit   | 1    | 75    |
| 4       | Sanvi | 1    | 80    |
| 6       | Riya  | 2    | 85    |
| 8       | Diya  | 1    | 90    |
____
## EHF Lecture
In this lecture we studied about CIA Triad and some security models
list of security models 
1. Bell-LaPadula
2. Biba Model
3. Clark-Wilson Model
4. Brewaer Model

___
## DBMS Lab 

we used the conditional queries on the existing tables with the LIKE operator
- Used to get the data from employee table where name of employee is having first letter `A` and third letter `a`
 ```SQL 
 SELECT * FROM EMPLOYEE WHERE EMP_NAME LIKE 'A_a%';
 ```
 - select emp_no , emp_name , emp_sal where emp_name is like 'Ani___'
 - select *  from employee where where emp_contact isnot null and emp_name is like '_n____';
 - select * from employee where dept like '%\_%' escape '\';
___
## IDT Lecture

- Ma'am discussed common computer science problems and their possible solutions.