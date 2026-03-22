# EXPERIMENT 3
## 1. Find all the Toy story movies.
```
SELECT *
FROM movies
WHERE title LIKE 'Toy Story%';
```
## 2. Find all the movies directed by john Lasseter
```
SELECT *
FROM movies
WHE./RE director = "John Lasseter"
```
## 3. Find all the movies (and director) not directed by John Lasseter
```
SELECT title, director
FROM movies
WHERE director != 'John Lasseter';
```
## 4. Find all the WALL-* movies
```
SELECT *
FROM movies
WHERE title LIKE 'WALL-%';
```
