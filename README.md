# Spotify-Data-Analysis-using-SQL

![spotify_logo](https://github.com/user-attachments/assets/eaf081e0-62bd-4ba2-8b7c-a04c53052e16)



# Overvew

This project focuses on analyzing a Spotify dataset containing various attributes related to tracks, albums, and artists using SQL. The process involves normalizing a denormalized dataset, executing SQL queries of varying complexity (ranging from simple to advanced), and optimizing query performance. The main objectives of the project are to enhance advanced SQL skills and extract meaningful insights from the dataset.L. 


![schema](https://github.com/user-attachments/assets/b9751837-4948-423e-923a-af130c41646f)

# Objectives

The primary objective of this SQL project is to analyze a Spotify dataset by leveraging advanced SQL techniques to derive meaningful insights. The project involves normalizing a denormalized dataset to ensure data integrity and optimize performance. It focuses on executing SQL queries of varying complexity, ranging from simple aggregations to advanced queries, such as using window functions, subqueries, and Common Table Expressions (CTEs). Key tasks include analyzing track attributes such as danceability, energy, and tempo, identifying popular tracks, albums, and artists based on views, streams, likes, and comments, and performing attribute-specific analyses to gain deeper insights. Additionally, the project aims to enhance query performance and efficiency while exploring advanced SQL skills to extract actionable insights from the dataset.


# Project Steps

1. Data Exploration
Before diving into SQL, it’s important to understand the dataset thoroughly. The dataset contains attributes such as:

Artist: The performer of the track.

Track: The name of the song.

Album: The album to which the track belongs.

Album_type: The type of album (e.g., single or album).

Various metrics such as danceability, energy, loudness, tempo, and more.

4. Querying the Data
   
After the data is inserted, various SQL queries can be written to explore and analyze the data. Queries are categorized into easy, medium, and advanced levels to help progressively develop SQL proficiency.

Easy Queries

Simple data retrieval, filtering, and basic aggregations.

Medium Queries

More complex queries involving grouping, aggregation functions, and joins.

Advanced Queries

Nested subqueries, window functions, CTEs, and performance optimization.

5. Query Optimization
   
In advanced stages, the focus shifts to improving query performance. Some optimization strategies include:

Indexing: Adding indexes on frequently queried columns.

Query Execution Plan: Using EXPLAIN ANALYZE to review and refine query performance.


# 15 Practice Questions

--- 1. Retrieve the names of all tracks that have more than 1 billion streams.

SELECT track 
FROM spotify
WHERE stream > 1000000000;

--- 2. List all albums along with their respective artists

SELECT album, artist 
FROM spotify ;

--- 3. Get the total number of comments for tracks where licensed = TRUE.

SELECT SUM(comments) AS total_comments 
FROM spotify
WHERE licensed = 1 ;

--- 4.  Find all tracks that belong to the album type single.

SELECT  track 
FROM spotify
WHERE album_type = 'single';

--- 5. Count the total number of tracks by each artist.

SELECT  artist,  COUNT(track) AS total_tracks 
FROM  spotify
GROUP BY artist;

===== Medium Level

--- 6. Calculate the average danceability of tracks in each album.

SELECT album, round(AVG(danceability),2) AS avg_danceability 
FROM spotify
GROUP BY album;

--- 7. Find the top 5 tracks with the highest energy values.

SELECT top 5  track, round(energy ,2) as Energy
FROM spotify
ORDER BY energy DESC;

--- 8. List all tracks along with their views and likes where official_video = 1 .

SELECT  track, views, likes 
FROM spotify
WHERE official_video = 1 ;

--- 9. For each album, calculate the total views of all associated tracks.

SELECT album, SUM(CAST(views AS BIGINT)) AS total_views
FROM spotify
GROUP BY album;

--- 10. Retrieve the track names that have been streamed on Spotify more than YouTube.

SELECT track 
FROM spotify
WHERE stream > views;

=== Advanced Level

--- 11. Find the top 3 most-viewed tracks for each artist using window functions.

SELECT  artist,  track,  views 
FROM ( SELECT artist, track, views, 
       ROW_NUMBER() OVER (PARTITION BY artist ORDER BY views DESC) AS rank 
       FROM  spotify) ranked_tracks
WHERE 
    rank <= 3;

--- 12. Write a query to find tracks where the liveness score is above the average.

SELECT track,  liveness 
FROM spotify
WHERE  liveness > (SELECT AVG(liveness) FROM spotify);

--- 13. Use a WITH clause to calculate the difference between the highest and lowest energy values for tracks in each album.

WITH energy_diff AS (
    SELECT album, MAX(energy) AS max_energy, MIN(energy) AS min_energy 
    FROM spotify
    GROUP BY album )
SELECT 
    album, (max_energy - min_energy) AS energy_difference 
FROM  energy_diff;



