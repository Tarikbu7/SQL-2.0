📌 Chapter 1 – Summary

This chapter explains how to query a SQL database to select, filter, and sort data.

🔹 Main SQL Clauses

SELECT: retrieves data from a table.

WHERE: filters results based on conditions.

ORDER BY: sorts results (ASC = ascending, DESC = descending).

LIMIT: restricts the number of returned rows.

🔹 Common Operators

=, <, >, >=

LIKE for pattern matching

🔹 Key Example
SELECT title, publish_date
FROM Article
WHERE user_id = 1
ORDER BY publish_date DESC;


➡️ Displays articles written by user 1, from newest to oldest.

🔹 Key Takeaways

SELECT * retrieves all columns.

WHERE filters data using conditions.

ORDER BY organizes results.

LIMIT controls how many results are shown.