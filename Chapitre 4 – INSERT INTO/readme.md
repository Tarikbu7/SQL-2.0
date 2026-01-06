Database Creation

Creates a new database called BlogDB and selects it for use.

Tables Setup

Utilisateur table: stores user information with fields for ID, name, email (unique), and password.

Article table: stores blog articles with fields for ID, content, publication date (default = current timestamp), and a foreign key linking each article to a user.

Data Insertion

Adds one article: “Bienvenue sur le blog” with content “Ceci est le premier article.” published on 2025‑07‑18 by user ID 1.

Adds three users:

Alice (alice@test.com, password 1234)

Bob (bob@test.com, password passbob)

Charlie (charlie@test.com, password passcharlie)

insert three articles

iNSERT INTO Article (contenu, date_publication, id_utilisateur) VALUES

('alice' 'Ceci est le premier article.', '2025-07-18', 1);

('Bob\'s first blog post.', '2025-07-19', 2),

('Charlie\'s thoughts on SQL.', '2025-07-20', 3),

