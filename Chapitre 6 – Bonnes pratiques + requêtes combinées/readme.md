Chapter 6 – Best Practices & Combined SQL Queries
🎯 Learning objective

Learn how to write optimized and secure SQL queries, combine multiple operations in one script, and use transactions to protect data consistency.

📚 Concepts covered

Combined queries (multiple SQL operations in one script)

SQL transactions:

START TRANSACTION

COMMIT

ROLLBACK

Best practices for readable SQL

Using comments:

-- single line

/* multi-line */

Security rules:

avoid unfiltered destructive queries

always use WHERE in UPDATE and DELETE

🧠 Theory

A transaction groups several operations into one logical unit.

START TRANSACTION → begins the transaction

COMMIT → permanently saves changes

ROLLBACK → cancels all changes made since the transaction started

They ensure:

data consistency

error recovery

safe multi-step operations

🧩 Example full script
START TRANSACTION;

INSERT INTO Article (title, content, publish_date, user_id)
VALUES ('Test article', 'Test content', '2025-07-18', 1);

UPDATE User
SET email = 'test@test.com'
WHERE id = 1;

DELETE FROM Comment
WHERE id = 2;

COMMIT;


If an error occurs → replace COMMIT with ROLLBACK.

🛠 Practical tutorial steps

Add comments

-- Script to manage blog data


Start transaction

START TRANSACTION;


Combine operations

insert

update

delete

Validate or cancel

COMMIT;

or ROLLBACK;

Verify result

SELECT * FROM Article;

🧾 Key takeaways

Use transactions for complex modifications

COMMIT saves changes

ROLLBACK undoes them

Always add comments

Avoid destructive queries without WHERE

Test deletes and updates with SELECT first