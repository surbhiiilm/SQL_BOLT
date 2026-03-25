# <CENTER> EXPERIMENT 10
## 1. Find the longest time that an employee has been at the studio
```SQL
SELECT MAX(YEAR(CURDATE()) - YEAR(employees.hire_date)) AS longest_years
FROM employees;
```
## 2. For each role, find the average number of years employed by employees in that role
```SQL
SELECT employees.role,
AVG(YEAR(CURDATE()) - YEAR(employees.hire_date)) AS avg_years
FROM employees
GROUP BY employees.role;
```
## 3. Find the total number of employee years worked in each building
```SQL
SELECT buildings.building_name,
SUM(YEAR(CURDATE()) - YEAR(employees.hire_date)) AS total_years
FROM employees
JOIN buildings
ON employees.building_id = buildings.building_id
GROUP BY buildings.building_name;
```