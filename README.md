# Shows-and-Movies-SQL
This project is a SQL-based database system designed to store, manage, and query information related to movies, TV shows, actors, directors, genres, ratings, and streaming platforms. It demonstrates end-to-end database design — including ER modeling, schema creation, normalization, and complex SQL queries.
🚀 Features
🔹 1. Well-Designed Database Schema

Movies and TV Shows data stored in structured tables

Separate tables for Actors, Directors, Genres, Platforms, Ratings

Proper primary keys, foreign keys, constraints, and relationships

🔹 2. Normalized Structure

Database normalized up to 3NF

Removes redundancy and ensures efficient data handling

🔹 3. Advanced SQL Queries

Includes SQL queries such as:

Fetching top-rated movies

Finding shows by genre

Listing movies by a specific director

Actor–Movie relationship queries

Platform-wise streaming availability

Aggregations, joins, nested queries, and grouping

🔹 4. ER Diagram Included

Shows all entities and relationships clearly, such as:

Movie ↔ Genre (Many-to-Many)

Movie ↔ Actor (Many-to-Many)

Movie ↔ Director (One-to-Many)

Movie ↔ Platform (Many-to-Many)

🔹 5. Sample Dataset

Inserted sample values for:

20+ Movies

10+ TV Shows

Actors, directors, genres, and streaming platforms
Makes testing easy.

🛠️ Tech Stack
Component	Description
SQL	MySQL / PostgreSQL / SQLite (any supported)
DB Tools	MySQL Workbench / pgAdmin / SQL CLI
Diagram Tools	Draw.io / ERDPlus
📂 Project Structure
📁 Shows-and-Movies-SQL
│── 📄 schema.sql        # Database structure (tables + constraints)
│── 📄 insert_data.sql   # Sample data for all tables
│── 📄 queries.sql       # Advanced SQL queries
│── 📄 er_diagram.png    # ER diagram of the database
│── 📄 README.md         # Project documentation

📊 Example SQL Queries
1️⃣ Get top 5 rated movies
SELECT title, rating
FROM Movies
ORDER BY rating DESC
LIMIT 5;

2️⃣ List all actors in a given movie
SELECT a.actor_name
FROM Actors a
JOIN Movie_Actor ma ON a.actor_id = ma.actor_id
JOIN Movies m ON m.movie_id = ma.movie_id
WHERE m.title = 'Inception';

3️⃣ Movies available on Netflix
SELECT m.title
FROM Movies m
JOIN Movie_Platform mp ON m.movie_id = mp.movie_id
JOIN Platforms p ON mp.platform_id = p.platform_id
WHERE p.name = 'Netflix';

🎯 Learning Outcomes

By completing this project, you will gain hands-on experience with:

Relational database design

ER modeling and normalization

SQL DDL & DML commands

Writing optimized and meaningful SQL queries

Handling many-to-many and one-to-many relationships

Real-world database project structure

📌 Use Cases

Movie recommendation systems

Streaming platform databases

OTT analytics

Education (DBMS learning project)

Resume / Portfolio enhancement
