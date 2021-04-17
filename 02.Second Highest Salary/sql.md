```
Create table If Not Exists Employee (Id int, Salary int);
Truncate table Employee;
insert into Employee (Id, Salary) values ('1', '100');
insert into Employee (Id, Salary) values ('2', '200');
insert into Employee (Id, Salary) values ('3', '300');
```

> Write a SQL query to get the second highest salary from the Employee table. If there is no second highest salary, then the query should return null.

```
select max(salary) as secondhighestsalary
from employee
where salary < (select max(salary) from employee);
```