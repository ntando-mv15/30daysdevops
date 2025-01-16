# NBADataLake Project
This repository contains the setup_nba_data_lake.py script, which automates the creation of a data lake for NBA analytics using AWS services. The script integrates Amazon S3, AWS Glue, and Amazon Athena, and sets up the infrastructure needed to store and query NBA-related data.

## Overview
The setup_nba_data_lake.py script performs the following actions:

- Creates an Amazon S3 bucket to store raw and processed data.
- Uploads sample NBA data (JSON format) to the S3 bucket.
- Creates an AWS Glue database and an external table for querying the data.
- Configures Amazon Athena for querying data stored in the S3 bucket.

## Tech Stack

- Language: Python 3x
- AWS Services: S3, Glue, Athena, IAM


## Project Documentation

Find detailed project documentation here: [NBA Data Lake Medium Article](https://medium.com/@ntando.mv15/sports-analytics-data-lake-project-e5636c43d707)


