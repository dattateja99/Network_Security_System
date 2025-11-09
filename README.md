# 🛡️ Network Security Project for Phishing Data

An end-to-end **MLOps-enabled Network Security System** built to detect phishing activity using machine learning and automated deployment pipelines.  
This project integrates **ETL pipelines**, **MLflow experiment tracking**, **GitHub Actions CI/CD**, **FastAPI model serving**, and **AWS Cloud Infrastructure** for scalable, reproducible security analytics.

---

## 🚀 Overview

The system automates every stage of a phishing detection workflow — from data ingestion and preprocessing to model training, versioning, deployment, and monitoring.

**Key Features**
- Automated ETL pipeline for cleaning and transforming phishing datasets.
- Model training with MLflow experiment tracking and versioning.
- CI/CD integration with GitHub Actions to trigger retraining and redeployment.
- FastAPI microservice for real-time phishing detection.
- Containerized deployment using Docker on AWS EC2.
- Artifact and data storage managed through AWS S3.
- Metadata and results stored in MongoDB for easy querying and analysis.

---

## 🧠 Tech Stack

| Component | Technology |
|------------|-------------|
| **ETL & ML** | Python, Pandas, Scikit-learn |
| **MLOps & Tracking** | MLflow, DagsHub |
| **CI/CD** | GitHub Actions |
| **Deployment** | FastAPI, Docker, AWS EC2 |
| **Storage** | AWS S3 (artifacts), MongoDB (metadata) |

---

## ⚙️ Architecture
    +-------------------+
    |    Phishing Data  |
    +---------+---------+
              |
              v
    +-------------------+
    |   ETL Pipeline    |  --> Cleaned data to S3
    +-------------------+
              |
              v
    +-------------------+
    |  Model Training   |  --> MLflow logs, metrics
    +-------------------+
              |
              v
    +-------------------+
    |  GitHub Actions   |  --> CI/CD automation
    +-------------------+
              |
              v
    +-------------------+
    |   Docker Image    |
    |   (FastAPI App)   |
    +-------------------+
              |
              v
    +-------------------+
    |  AWS EC2 Hosting  |
    |  & MongoDB Store  |
    +-------------------+
---

## 🧩 Key Components

### 1. **ETL Pipeline**
Automates extraction, cleaning, and transformation of phishing datasets before feature engineering and model training.  
The processed data is stored in AWS S3 and version-controlled for reproducibility.

### 2. **Model Training & MLflow**
Tracks experiments, hyperparameters, and metrics using MLflow.  
Best-performing models are automatically logged and registered for deployment.

### 3. **CI/CD with GitHub Actions**
Automates:
- Model retraining on new data commits  
- Docker image builds and pushes  
- FastAPI app deployment to EC2  

### 4. **FastAPI Inference Service**
Exposes a `/predict` endpoint for real-time phishing URL classification.

### 5. **Monitoring**
Metrics such as request latency and prediction drift are logged to MLflow and MongoDB.  
System health and performance are monitored using AWS tools.

---
