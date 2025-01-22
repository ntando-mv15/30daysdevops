# 30 Days DevOps Challenge - Weather Dashboard

Day 1: Building a weather data collection system using AWS S3 and OpenWeather API

# Weather Data Collection System - DevOps Day 1 Challenge

## Project Overview
This project is a Weather Data Collection System that demonstrates core DevOps principles by combining:
- External API Integration (OpenWeather API)
- Cloud Storage (AWS S3)
- Version Control (Git)
- Python Development
- Environment Management

## Features
- Fetches real-time weather data for multiple cities
- Displays temperature (°F), humidity, and weather conditions
- Automatically stores weather data in AWS S3
- Supports multiple cities tracking

## Technical Architecture
- **Language:** Python 3.x
- **Cloud Provider:** AWS (S3)
- **External API:** OpenWeather API

- **Dependencies:** 
  - boto3 (AWS SDK)
  - python-dotenv
  - requests

## Project Structure

## **Project Structure**
```bash
day01-weather-dashboard//
├── src/
│   ├── __init__.py 
    ├── weather_dashboard.py         # Main Python function code
├── .gitignore
├── README.md                        # Project documentation
└── requirements.txt                 # Project dependencies
```


weather-dashboard/
├── src/
│   ├── init.py
│   └── weather_dashboard.py
├── tests/
├── data/
├── .env
├── .gitignore
└── requirements.txt

## Setup Instructions
1. Clone the repository:

    ```bash
    git clone 
    ```

3. Install dependencies:
    ```bash
    pip install -r requirements.txt
    ```

4. Configure environment variables (.env):

    ```
    OPENWEATHER_API_KEY=your_api_key
    AWS_BUCKET_NAME=your_bucket_name
    ```

4. Configure AWS credentials:

    ```bash
    aws configure
    ```

5. Run the application:

    ```bash
    python src/weather_dashboard.py
    ```

## Project Documentation
Find Detailed Project Documentation Here: [Weather Data Collection System Medium Article](https://medium.com/@ntando.mv15/a-weather-data-collection-system-with-openweather-api-and-aws-s3-a1fcc90f5e82)

## What I Learned:

- AWS S3 bucket creation and management
- Environment variable management for secure API keys
- Python best practices for API integration
- Git workflow for project development
- Cloud resource management

