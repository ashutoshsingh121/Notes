# Notes

SQL QueryBook


Perform All Query on https://livesql.oracle.com/


1. Select employee_id, first_name and effective salary after increasing by 8%.
> select employee_id, first_name, salary + salary*8/100 as new_salary from hr.employees;

2. Select employee_id, first_name and salaries greater than 10000.
> select employee_id, first_name,salary from hr.employees where salary > 10000;


3. Select employee_id, first_name and salaries lesser than 100000.
> select employee_id, first_name,salary from hr.employees where salary < 100000;


4. Select employee_id, first_name and salaries equal to 24000.
> select employee_id, first_name,salary from hr.employees where salary = 24000;


5. Select employee_id, first_name and salaries not equal to 17000.
> select employee_id, first_name,salary from hr.employees where salary <> 17000;

> select employee_id, first_name,salary from hr.employees where salary != 17000;



6. Select employee_id, first_name, salary less than 10000 and job_id is ‘IT_PROG’
> select employee_id, first_name, salary, job_id from hr.employees where salary < 10000 and job_id = 'IT_PROG';



7. Select employee_id, first_name, manager_id is 100 or department_id is 100.
> select employee_id, first_name, manager_id, department_id from hr.employees where manager_id = 100 or department_id = 100;


8. Select employee_id, first_name and department_id should be 80 or 90 or 100.
> select employee_id, first_name, department_id from hr.employees where department_id in (80,90,100);


9. Select employee_id, first_name and department_id should not be 80 or 90 or 100.
> select employee_id, first_name, department_id from hr.employees where department_id not in (80,90,100);


10. Select employee_id, salary if salary is greater than 10000 and less than 50000.
> select employee_id, salary from hr.employees where salary between 10000 and 50000;


11. Select employee_id, first_name and commission_pct which are not null.
> select employee_id, first_name, commission_pct from hr.employees where commission_pct is not null;

12.. Select employee_id, first_name and commission_pct which are null.
> select employee_id, first_name, commission_pct from hr.employees where commission_pct is null;


13. Select employee_id, first_name and all the commission_pct and make sure to show null values as 0.
> select employee_id, first_name, NVL(commission_pct,0) from hr.employees;


14. Select employee_id, first_name and all the commission_pct and make sure to show null values as 0 and non-null values as 1.
> select employee_id, first_name, NVL2(commission_pct,1,0) from hr.employees;


15. Select the employee having max salary.
> select max(salary) from hr.employees;


16. Select the employee having min salary.
> select min(salary) from hr.employees;


17. Select the employee’s average salary.
> select avg(salary) from hr.employees;


18. Select the sum of employee’s salary.
> select sum(salary) from hr.employees;


19. Select the count of employees having a commission_pct.
> select count(commission_pct) from hr.employees;


20. Show avg salaries of each department
> select department_id, avg(salary) from hr.employees group by department_id;

21. Show count of managers and avg salaries for each department which is not null
> select department_id, count(manager_id), avg(salary) from hr.employees where department_id is not null group by department_id;

> select department_id, count(manager_id), avg(salary) from hr.employees group by department_id having department_id is not null;


22. Sort the grouped departments in ascending order
> select department_id, count(manager_id), avg(salary) from hr.employees group by department_id order by department_id;

