# EXPERIMENT 3
## 1. Find all the Toy story movies.
```sql
SELECT *
FROM movies
WHERE title LIKE 'Toy Story%';
```
## 2. Find all the movies directed by john Lasseter
```sql
SELECT *
FROM movies
WHE./RE director = "John Lasseter"
```
## 3. Find all the movies (and director) not directed by John Lasseter
```sql
SELECT title, director
FROM movies
WHERE director != 'John Lasseter';
```
## 4. Find all the WALL-* movies
```sql
SELECT *
FROM movies
WHERE title LIKE 'WALL-%';
```
