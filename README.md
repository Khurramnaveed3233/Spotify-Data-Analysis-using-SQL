# Spotify-Data-Analysis-using-SQL

![spotify_logo](https://github.com/user-attachments/assets/eaf081e0-62bd-4ba2-8b7c-a04c53052e16)



# Overvew

This project focuses on analyzing a Spotify dataset containing various attributes related to tracks, albums, and artists using SQL. The process involves normalizing a denormalized dataset, executing SQL queries of varying complexity (ranging from simple to advanced), and optimizing query performance. 

The main objectives of the project are to enhance advanced SQL skills and extract meaningful insights from the dataset.L. 


![schema](https://github.com/user-attachments/assets/b9751837-4948-423e-923a-af130c41646f)

## Objectives

The primary objective of this SQL project is to analyze a Spotify dataset by leveraging advanced SQL techniques to derive meaningful insights. The project involves normalizing a denormalized dataset to ensure data integrity and optimize performance. It focuses on executing SQL queries of varying complexity, ranging from simple aggregations to advanced queries, such as using window functions, subqueries, and Common Table Expressions (CTEs). 

Key tasks include analyzing track attributes such as danceability, energy, and tempo, identifying popular tracks, albums, and artists based on views, streams, likes, and comments, and performing attribute-specific analyses to gain deeper insights. Additionally, the project aims to enhance query performance and efficiency while exploring advanced SQL skills to extract actionable insights from the dataset.


# Project Steps

# 1. Data Exploration
Before diving into SQL, it’s important to understand the dataset thoroughly. The dataset contains attributes such as:

- **Artist:** The performer of the track.

- **Track:** The name of the song.

- **Album:** The album to which the track belongs.

- **Album_type:** The type of album (e.g., single or album).

Various metrics such as danceability, energy, loudness, tempo, and more.

# 4. Querying the Data
   
After the data is inserted, various SQL queries can be written to explore and analyze the data. Queries are categorized into easy, medium, and advanced levels to help progressively develop SQL proficiency.

- **Easy Queries**
  - Simple data retrieval, filtering, and basic aggregations.

- **Medium Queries**
  - More complex queries involving grouping, aggregation functions, and joins.

- **Advanced Queries**
  - Nested subqueries, window functions, CTEs, and performance optimization.

# 5. Query Optimization
   
In advanced stages, the focus shifts to improving query performance. Some optimization strategies include:

- **Indexing:** Adding indexes on frequently queried columns.

- **Query Execution Plan:**  Using EXPLAIN ANALYZE to review and refine query performance.


# Business Problems and Solutions

- 1. Retrieve the names of all tracks that have more than 1 billion streams
   
![1](https://github.com/user-attachments/assets/5a2f1978-c73a-4307-a69b-f03e22e6921b)

2. List all albums along with their respective artists

![2](https://github.com/user-attachments/assets/91393ba3-e481-4418-ad62-22d2aee0ed9b)

3. Get the total number of comments for tracks where licensed = 1 .

![3](https://github.com/user-attachments/assets/3524a999-59e4-4a3f-a357-79ac6afc1415)

4.  Find all tracks that belong to the album type single

![4](https://github.com/user-attachments/assets/09d82115-82c9-4f09-b5b9-fb18d58c0ca1)

5. Count the total number of tracks by each artist.

![5](https://github.com/user-attachments/assets/87ab84d4-7824-4961-a3f3-844a641b4f15)

6. Calculate the average danceability of tracks in each album

![6](https://github.com/user-attachments/assets/10352e75-f9bc-46b5-aa2c-25e406c29b9f)

7. Find the top 5 tracks with the highest energy values
   
![7](https://github.com/user-attachments/assets/5d3108e3-8ffe-495d-8c0d-7927f0649f25)

8. List all tracks along with their views and likes where official_video = 1

![8](https://github.com/user-attachments/assets/a07b3fe6-f44b-4fd4-bf05-4e6bd9649640)

9. For each album, calculate the total views of all associated tracks.

![9](https://github.com/user-attachments/assets/b92743ee-715d-4429-b75b-1122f0058519)

10. Retrieve the track names that have been streamed on Spotify more than YouTube.

![10](https://github.com/user-attachments/assets/afdfeb8e-af8e-431c-9c35-1bad29c99cb7)

11. Find the top 3 most-viewed tracks for each artist using window functions.

![11](https://github.com/user-attachments/assets/7bd8485f-1c20-44c9-906f-35cdb5f40249)

12. Write a query to find tracks where the liveness score is above the average.

![12](https://github.com/user-attachments/assets/3a073cd7-2c15-40d2-8217-77adb3fed740)

13. Use a WITH clause to calculate the difference between the highest and lowest energy values for tracks in each album.

![13](https://github.com/user-attachments/assets/a257b69e-d12f-4d6f-b694-251ff7e521a8)

# Findings and Conclusion

Findings:

1. Most Popular Tracks and Artists:

     The tracks with the highest views and streams were identified, revealing the most popular songs on Spotify. Artists with the most tracks and highest overall engagement (views, 
     likes, and comments) were also highlighted.
   
     
2. Track and Album Characteristics:

     Tracks with specific characteristics, such as high danceability, energy, or liveness, were analyzed. Albums classified as "single" were found to represent a significant portion of 
     the dataset.

3. Engagement Metrics:

    Tracks with official videos showed a clear correlation with higher engagement, as evidenced by increased views and likes.

Advanced Insights Using Window Functions:

    Window functions provided rankings for the top 3 most-viewed tracks for each artist, giving deeper insights into artist-specific performance.

Statistical Analysis:

   The average danceability of tracks across different albums and the variation in energy levels were calculated, offering insights into musical trends and styles.

Normalization Benefits:

    Normalizing the dataset improved query efficiency and reduced data redundancy, enhancing the overall quality of analysis.

Liveness and Streaming Platforms:

    Tracks with above-average liveness scores were identified, and those streamed more on Spotify than YouTube highlighted platform-specific preferences.

# Conclusion:

This project demonstrated the power of SQL in analyzing and extracting insights from large datasets. By performing a range of queries, from simple aggregations to advanced window functions, we were able to uncover meaningful trends in track popularity, artist performance, and track characteristics. 

The normalization of the dataset significantly improved the efficiency of querying and ensured data accuracy. The insights derived from this analysis can be leveraged to understand listener preferences, optimize content strategies, and enhance user engagement on music streaming platforms. 

This project also provided hands-on experience in advanced SQL techniques, solidifying the understanding of query optimization and complex data analysis.

# This Project is designed and made by Khurram Naveed using SQL

This project is part of my portfolio, showcasing the SQL skills essential for data analyst roles. If you have any questions, feedback, or would like to collaborate, feel free to get in touch


