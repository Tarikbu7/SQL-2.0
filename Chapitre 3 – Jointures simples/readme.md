chapter 3 – SQL Joins
🎯 Objective

Learn how to combine multiple tables to display merged data using SQL joins.

📚 Concepts Covered

The concept of joining tables

INNER JOIN (inner join)

LEFT JOIN and RIGHT JOIN (outer joins)

Using aliases to simplify queries

Filtering data after a join

🧠 Theory

Joins allow you to combine data from multiple tables linked by primary and foreign keys:

INNER JOIN: returns only rows that have matching values in both tables.

LEFT JOIN: returns all rows from the left table, even if there’s no match in the right table.

RIGHT JOIN: returns all rows from the right table, even if there’s no match in the left table.

Example: Display articles with the author’s name

SELECT a.title, u.name
FROM Article a
INNER JOIN User u ON a.user_id = u.id;

🛠 Practical Tutorial
1️⃣ Basic INNER JOIN

Display the title, publication date, and author name:

SELECT a.title, a.pub_date, u.name
FROM Article a
INNER JOIN User u ON a.user_id = u.id;

2️⃣ Add a filter

Show only articles written by Alice:

SELECT a.title, u.name
FROM Article a
INNER JOIN User u ON a.user_id = u.id
WHERE u.name = 'Alice';

3️⃣ LEFT JOIN to see articles without authors
SELECT a.title, u.name
FROM Article a
LEFT JOIN User u ON a.user_id = u.id;

4️⃣ Join with 3 tables

Display articles, authors, and comments:

SELECT a.title, u.name, c.content
FROM Article a
INNER JOIN User u ON a.user_id = u.id
INNER JOIN Comment c ON a.id = c.article_id;
🧾 Key Points

Joins link tables via primary and foreign keys.

INNER JOIN: only matching rows are returned.

LEFT JOIN: all rows from the main table are kept, even without matches.

Aliases (a, u, c) make queries shorter and easier to read.