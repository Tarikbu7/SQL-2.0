Chapter 5 – UPDATE and DELETE
🎯 Learning objective

Be able to modify and delete records in an SQL table using the UPDATE and DELETE commands while applying precise conditions to avoid mistakes.

📚 Key concepts

Syntax of UPDATE and DELETE

Mandatory use of WHERE to target specific rows

Updating one or multiple columns

Conditional or complete deletion of data

Precautions and backups before deleting data

🧠 Theory

UPDATE is used to change values in one or more columns.

DELETE is used to remove rows from a table.

⚠ Without WHERE, all rows will be affected (risk of total update or deletion).

🛠 Practical examples

Update one user

UPDATE Utilisateur
SET nom = 'Alice Dupont', email = 'alice.dupont@test.com'
WHERE id = 1;


Update multiple rows

UPDATE Article
SET titre = 'Updated article'
WHERE id_utilisateur = 1;


Delete one record

DELETE FROM Commentaire
WHERE id = 2;


Delete multiple records

DELETE FROM Article
WHERE date_pub < '2024-01-01';


Check results

SELECT * FROM Utilisateur;
SELECT * FROM Article;

🧾 Key takeaways

UPDATE modifies data according to a condition.

DELETE removes rows; never forget WHERE unless you really want everything deleted.

Always test with SELECT first before large updates or deletions.

Make a backup before important deletions.