# Spotify Advanced SQL Analytics

Advanced SQL analytics project using PostgreSQL to analyze Spotify listening data, derive business insights, and optimize query performance through indexing and execution plan analysis.

**Dataset:** https://www.kaggle.com/datasets/sanjanchaudhari/spotify-dataset

![Spotify Logo](spotify_logo.jpg)

---

# Overview

This project explores Spotify listening data using advanced SQL techniques to analyze artist, album, and track performance. It demonstrates SQL concepts ranging from basic aggregations to advanced analytical queries while showcasing query optimization using indexing and `EXPLAIN ANALYZE`.

The project includes:

- 15 analytical SQL problems
- CTEs and Window Functions
- Aggregations and Subqueries
- Query Optimization
- Execution Plan Analysis

---

# Database Schema

```sql
DROP TABLE IF EXISTS spotify;

CREATE TABLE spotify (
...
);
```

---

# Dataset Overview

The dataset contains information including:

- Artist
- Track
- Album
- Album Type
- Views
- Streams
- Likes
- Comments
- Danceability
- Energy
- Loudness
- Tempo
- Acousticness
- Liveness
- Valence
- Platform information

---

# SQL Practice Questions

The project contains **15 SQL problems** grouped by difficulty.

## Easy

*(keep your existing questions exactly as they are)*

---

## Medium

*(keep existing queries)*

---

## Advanced

*(keep existing queries)*

---

# Query Optimization

To improve query performance, indexing was implemented on the `artist` column and execution plans were compared before and after optimization.

## Before Indexing

Execution Time: **7 ms**

Planning Time: **0.17 ms**

![EXPLAIN Before Index](spotify_explain_before_index.png)

---

## Creating the Index

```sql
CREATE INDEX idx_artist ON spotify_tracks(artist);
```

---

## After Indexing

Execution Time: **0.153 ms**

Planning Time: **0.152 ms**

![EXPLAIN After Index](spotify_explain_after_index.png)

---

## Performance Comparison

The charts below illustrate the reduction in execution time after indexing.

![Performance Comparison](spotify_graphical view 1.png)

![Performance Comparison](spotify_graphical view 2.png)

![Performance Comparison](spotify_graphical view 3.png)

---

# Technologies Used

- PostgreSQL
- SQL
- pgAdmin 4
- EXPLAIN ANALYZE

---

# Repository Structure

```
Spotify-Advanced-SQL-Project
│
├── README.md
├── spotify_logo.jpg
├── spotify_explain_before_index.png
├── spotify_explain_after_index.png
├── spotify_graphical view 1.png
├── spotify_graphical view 2.png
└── spotify_graphical view 3.png
```

---

# Getting Started

1. Install PostgreSQL and pgAdmin.
2. Create the database using the provided schema.
3. Import the Spotify dataset.
4. Execute the SQL queries.
5. Compare execution plans before and after indexing.

---

# Future Improvements

- Build a Power BI dashboard using query outputs.
- Perform additional performance tuning.
- Analyze larger datasets for scalability.

---

# License

This project is licensed under the MIT License.
