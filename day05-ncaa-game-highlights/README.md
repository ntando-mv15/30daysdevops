# NCAAGameHighlights

# HighlightProcessor
This project uses RapidAPI to obtain NCAA game highlights using a Docker container and uses AWS Media Convert to convert the media file.

# File Overview

### The ```config.py``` script performs the following actions:
- Imports necessary environment variables and assigns them to Python variables, providing default values where appropriate. 
- This approach allows for flexible configuration management, enabling different settings for various environments (e.g., development, staging, production) without modifying the source code.

### The ```fetch.py``` script performs the following actions:

- Establishes the date and league that will be used to find highlights (we are using NCAA in this example because it's included in the free version).
- This will fetch the highlights from the API and store them in an S3 bucket as a JSON file (basketball_highlight.json).

### The ```process_one_video.py``` script performs the following actions:

- Connects to the S3 bucket and retrieves the JSON file.
- Extracts the first video URL from within the JSON file.
- Downloads the video file from the internet into the memory using the requests library.
- Saves the video as a new file in the S3 bucket under a different folder (videos/).
- Logs the status of each step.

### The ```mediaconvert_process.py``` script performs the following actions:

- Creates and submits a MediaConvert job
- Uses MediaConvert to process a video file - configures the video codec, resolution and bitrate. Also configured the audio settings
- Stores the processed video back into an S3 bucket

### The ```run_all.py``` script performs the following actions:
- Runs the scripts in a chronological order and provides buffer time for the tasks to be created.

### The ```.env``` file stores all over the environment variables, these are variables that we don't want to hardcode into our script.

### The ```Dockerfile``` performs the following actions:
- Provides the step by step approach to build the image.


# **Technical Diagram**
![GameHighlightProcessor](https://github.com/user-attachments/assets/762c3582-c6fe-48b2-b7da-0ff5b86b7970)

## **Project Structure**
```
day05-ncaa-game-highlights
├── resources/
│    ├── IAMPolicies
│    ├── ncaaprojectcleanup.sh
│    ├── vpc_setup.sh           
├── src/
│    ├── Dockerfile
│    ├── config.py
│    ├── fetch.py
│    ├── mediaconvert_process.py
│    ├── process_one_video.py
│    ├── requirements.txt
│    ├── run_all.py
│    ├── .env
│    ├── .gitignore
├── README.md
```


### **What We Learned**
1. Working with Docker and AWS Services
2. Identity Access Management (IAM) and least privilege
3. How to enhance media quality 

## **Project Documentation**

Find detailed project documentation here: [NCAA Game Highlights Medium Article](https://medium.com/@ntando.mv15/ncaa-game-highlights-processor-702d59d010bf)


### **Future Enhancements**
- Using Terraform to enhance the Infrastructure as Code (IaC).



