# Sports API Management System

## **Project Overview**
This project demonstrates building a containerized API management system for querying sports data. It makes use of **Amazon ECS (Fargate)** for running containers, **Amazon API Gateway** for exposing REST endpoints, and an external **Sports API** for real-time sports data. The project showcases advanced cloud computing practices, including API management, container orchestration, and secure AWS integrations.

---

## **Features**
- Exposes a REST API for querying real-time sports data
- Runs a containerized backend using Amazon ECS with Fargate
- Scalable and serverless architecture
- API management and routing using Amazon API Gateway

---

## **Project Structure**

```bash
sports-api-management/
├── app.py # Flask application for querying sports data
├── Dockerfile # Dockerfile to containerize the Flask app
├── requirements.txt # Python dependencies
├── .gitignore
└── README.md # Project documentation
```

---

## **Setup Instructions**

### **Clone the Repository**
```bash
git clone https://github.com/ifeanyiro9/containerized-sports-api.git
cd containerized-sports-api
```

## Project Documentation:

Find detailed project documentation here: [Medium Article](https://medium.com/@ntando.mv15/day-4-sports-api-management-system-5de9194460e0)

### **What We Learned**
Setting up a scalable, containerized application with ECS
Creating public APIs using API Gateway.




