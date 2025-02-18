# SportsDataBackup
The Sports Backup Highlights Project is an extension of Day 05, and it automates fetching sports highlights, stores data in S3 and DynamoDB, processes videos, and runs on a schedule using ECS Fargate and EventBridge. It uses templated JSON files with environment variable injection for easy configuration and deployment.

# Technical Diagram 

![alt text](<Screenshot 2025-02-18 094348-1.png>)

## Project Structure
```
day06-sports-data-backup
├── resources/
│    ├── vpc_setup.sh           
├── src/
│    ├── .env
│    ├── Dockerfile
│    ├── config.py
│    ├── ecsEventsRole-policy.template.json
│    ├── ecsEventsRole-trust.json
│    ├── ecsTarget.template.json
│    ├── fetch.py
│    ├── mediaconvert_process.py
│    ├── process_videos.py
│    ├── requirements.txt
│    ├── run_all.py
│    ├── s3_dynamodb_policy.template.json
│    ├── taskdef.template.json
├── README.md
```

### **What I Learned**
1. Using templates to generate json files
2. Integrating DynamoDB to store data backup
3. Using Cloudwatch for logging

## Project Documentation 

Find detailed project documentation here: [Sports Data Bacup Medium Article](https://medium.com/@ntando.mv15/automating-sports-highlights-backup-with-aws-ecs-eventbridge-9a31d91fd02d)

### **Future Enhancements**
1. Integrate exporting a table from DynamoDB to an S3 bucket
2. Creating batch processing of the entire Json file (importing more than 10 videos)
