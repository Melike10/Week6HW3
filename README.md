# PostgreSQL Queries - Patika.dev ASP.NET Core Assignment

This repository contains SQL queries related to the PostgreSQL database as part of the assignment for the Patika.dev ASP.NET Core course. The queries are designed to perform various operations on the `country` and `film` tables of a sample database.

## Queries Overview

### 1. Retrieve country names that start with 'A' and end with 'a'
```sql
SELECT country FROM country 
WHERE country LIKE 'A%a';
```

This query selects the country column from the country table where the country names start with 'A' and end with 'a'.

### 2. Retrieve country names that are at least 6 characters long and end with 'n'
```sql

SELECT country
FROM country
WHERE LENGTH(country) >= 6
  AND country LIKE '%n';
```

This query selects the country column from the country table where the country names are at least 6 characters long and end with 'n'.

### 3. Retrieve film titles that contain at least 4 occurrences of the character 'T' (case insensitive)
```sql

SELECT * FROM film
WHERE title ILIKE '%t%t%t%t%';
```
This query retrieves all columns from the film table where the title contains at least 4 occurrences of the character 'T', case insensitive.

### 4. Retrieve all columns from the film table where the title starts with 'C', the length is greater than 90, and the rental_rate is 2.99
```sql

SELECT * FROM film
WHERE title LIKE 'C%'
AND length > 90
AND rental_rate = 2.99;
```

This query returns all columns from the film table for rows where the title starts with 'C', the length is greater than 90, and the rental_rate is 2.99.

