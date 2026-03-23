# <CENTER> EXPERIMENT 8
## 1. Find the name and role of all employees who have not been assigned to a building
```SQL
SELECT Employees.name, Employees.role
FROM Employees
LEFT JOIN Buildings
ON Employees.building = Buildings.building_name
WHERE Buildings.building_name IS NULL;
```
## 2. Find the names of the buildings that hold no employees 
```SQL
SELECT Buildings.building_name
FROM Buildings
LEFT JOIN Employees
ON Buildings.building_name = Employees.building
WHERE Employees.building IS NULL;
```