# <CENTER> EXPERIMENT 7
## 1. Find the list of all buildings that have employees 
```SQL
SELECT Buildings.building_name
FROM Buildings
INNER JOIN Employees
ON Buildings.building_name = Employees.building;
```
## 2. Find the list of all buildings and their capacity
```SQL
SELECT Buildings.building_name, Buildings.capacity
FROM Buildings;
```
## 3. List all buildings and the distinct employee roles in each building (including empty buildings)
```SQL
SELECT Buildings.building_name, Employees.role
FROM Buildings
LEFT JOIN Employees
ON Buildings.building_name = Employees.building
GROUP BY Buildings.building_name, Employees.role;
```
