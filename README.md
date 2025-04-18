# Music-store-data-analysis-project

This repository documents my work on the Music Store Data Analysis project, which I completed using SQL. This project involved analyzing a digital music store's database to uncover insights and answer key business questions. It was a great way for me to apply and demonstrate my SQL skills on a realistic dataset.


## Project Goal
The main goal of this project was to use SQL queries to analyze the music store's data and provide insights that could help the business understand customer behavior, sales trends, and popular genres/artists.


## Dataset & Schema
The schema of music store data model consisted of several interconnected tables:
![MusicDatabaseSchema](https://github.com/thesmartlad/Music-store-data-analysis-project/blob/main/Music%20store%20database%20schema.png)

Understanding the relational structure and the Primary Key / Foreign Key relationships between these tables was crucial for constructing accurate queries.


## Technical Process & SQL Techniques Employed
### Database Setup & Environment:
- Set up a relational database environment in PostgreSQL
- Created the database schema based on the provided structure.
- Populated the tables with data, likely using SQL `INSERT` statements or importing from CSV/SQL dump files.

### Data Exploration & Querying Strategy:
- Started with basic `SELECT` statements to understand the data within individual tables.
- Progressively built more complex queries to answer specific business questions.
- Utilized pgAdmin database client for query execution and result visualization.

### Core SQL Techniques Applied:
- **JOIN Operations:** Extensively used `INNER JOIN` to combine data from related tables based on foreign key relationships (e.g., linking Invoice to Customer, InvoiceLine to Track, Track to Album, Album to Artist). 
  `LEFT JOIN` might have been used in specific scenarios to include all records from one table even if there's no match in the other.

- **Aggregate Functions:** Employed functions like `COUNT()`, `SUM()`, `AVG()` with the GROUP BY clause to summarize data (e.g., calculating total sales per city, counting invoices per country, finding average track 
  length).

- **Filtering Data:** Used the `WHERE` clause for filtering records based on specific criteria (e.g., selecting customers from a particular country, filtering for a specific genre like 'Rock').

- **Sorting Results:** Applied `ORDER BY` (with ASC/DESC) to arrange the output meaningfully (e.g., ranking cities by sales, ordering employees by hire date).

- **Limiting Results:** Used `LIMIT` to retrieve only the top N results (e.g., top 3 invoice values, top 10 rock artists).

- **Subqueries:** Implemented subqueries (queries nested inside another query) for multi-step logic, such as finding tracks longer than the overall average length or identifying customers who bought tracks from a 
  specific artist.

- **Common Table Expressions (CTEs):** Utilized `WITH` clauses (CTEs) to break down complex queries into logical, readable steps. This was particularly useful for advanced questions involving multiple joins and aggregations, like finding the most popular genre or top customer per country.

- **Window Functions (Potential Use):** For more complex ranking scenarios like finding the top customer within each country (`PARTITION BY` combined with ranking functions like `ROW_NUMBER()` or `RANK()`), window functions are the standard approach, likely demonstrated in the advanced questions.


## Key Questions Answered (Technical Perspective)
### Answering the project questions required applying the techniques above:

**Easy:** Primarily involved simple `SELECT`, `WHERE`, `ORDER BY`, `LIMIT`, and basic aggregate functions (`COUNT`, `SUM`) with `GROUP BY`.

**Moderate:** Required more complex `JOIN` operations across multiple tables, combining filtering with aggregations, and potentially using subqueries for filtering based on aggregated results (e.g., average track length).

**Advanced:** Necessitated intricate multi-table JOINs, extensive use of subqueries or CTEs for logical separation, and potentially window functions for partitioned ranking (e.g., finding the best customer per country).


## What I Learned & Key Findings
### This project solidified my understanding and practical application of:

- Relational database schema design and navigation.

- Crafting efficient SQL queries involving multiple tables.

- Using aggregate functions, subqueries, and CTEs to solve complex analytical problems.

- Translating business requirements into specific SQL queries.

The analysis yielded insights into customer spending habits, geographic sales distribution, and genre popularity, demonstrating the power of SQL for business intelligence.




