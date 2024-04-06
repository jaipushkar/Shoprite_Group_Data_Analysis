# Shoprite_Group_Data_Analysis

Shoprite Group Data Analysis
This repository contains a SQL query for analyzing data from the Shoprite Group, specifically from the Sample_ShopriteGroup_11_30_2023 table. The query retrieves distinct job numbers from the dataset where the job number matches '3333333' and aggregates them into a single string.

Overview
The provided SQL query focuses on extracting distinct job numbers from the Shoprite Group dataset dated November 30, 2023. It filters the data based on a specific job number ('3333333') and aggregates the distinct job numbers into a single string.

SQL Query
_**WITH pricerite AS (
    SELECT * FROM Sample_ShopriteGroup_11_30_2023 WHERE job_number = '3333333'
)
SELECT STRING_AGG(dist_job, ',') FROM (
    SELECT DISTINCT(job_number) AS dist_job FROM pricerite
) x;**_


Description
This SQL query facilitates the analysis of job numbers within the Shoprite Group dataset, aiding in identifying unique instances of a particular job number. By aggregating the distinct job numbers into a single string, users can efficiently track and manage data associated with specific jobs.

How to Use
Clone this repository to your local machine.
Execute the provided SQL query in your SQL Server environment, ensuring that you have access to the Sample_ShopriteGroup_11_30_2023 table.
Review the output to obtain the aggregated list of distinct job numbers matching the specified criteria.
