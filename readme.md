# Chapter 2 – Aggregate Functions & GROUP BY

## 🎯 Learning Objective
Learn how to use aggregate functions and the `GROUP BY` clause to group and analyze data in an SQL database.

## 📚 Concepts Covered
- Aggregate functions: `COUNT()`, `SUM()`, `AVG()`, `MIN()`, `MAX()`
- `GROUP BY` clause for grouping results
- `HAVING` clause to filter groups
- Difference between `WHERE` and `HAVING`
- Aggregation examples using an `Article` table

## 🧠 Theory Overview
Aggregate functions compute values from a set of rows (e.g., total articles, average views).
`GROUP BY` groups rows based on one or more columns.

- `WHERE` filters rows **before** aggregation
- `HAVING` filters results **after** aggregation

### Example
```sql
SELECT id_utilisateur, COUNT(*) AS nb_articles
FROM Article
GROUP BY id_utilisateur
HAVING COUNT(*) > 2;
