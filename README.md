# Notes

SQL QueryBook


Perform All Query on https://livesql.oracle.com/


1. Select employee_id, first_name and effective salary after increasing by 8%.
> select employee_id, first_name, salary + salary*8/100 as new_salary from hr.employees;

