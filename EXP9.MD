# <CENTER> EXPERIMENT 9
## 1. List all movies and their combined sales in millions of dollars
```SQL
SELECT Movies.title,
       (BoxOffice.domestic_sales + BoxOffice.international_sales) / 1000000 AS total_sales_millions
FROM Movies
INNER JOIN BoxOffice
ON Movies.id = BoxOffice.movie_id;
```
## 2. List all movies and their ratings in percent
```SQL
SELECT Movies.title,
       BoxOffice.rating * 10 AS rating_percent
FROM Movies
INNER JOIN BoxOffice
ON Movies.id = BoxOffice.movie_id;
```
## 3. List all movies that were released on even number years
```SQL
SELECT Movies.title, Movies.year
FROM Movies
WHERE Movies.year % 2 = 0;
```