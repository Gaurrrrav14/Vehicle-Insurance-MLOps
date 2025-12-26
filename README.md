# Vehicle Data MLOps Project

A **production-style MLOps pipeline** that demonstrates how to structure, build, train, evaluate, version, and deploy a machine learning system using **MongoDB, AWS, Docker, and CI/CD**.

This project focuses on **engineering workflows**, not just model training.

---

## What This Project Implements

* Modular Python project setup using `setup.py` and `pyproject.toml`
* Data storage and retrieval using **MongoDB Atlas**
* Structured logging and exception handling
* End-to-end ML pipeline:

  * Data Ingestion
  * Data Validation
  * Data Transformation
  * Model Training
  * Model Evaluation
  * Model Pusher
* Model registry using **AWS S3**
* Prediction pipeline with a web interface
* Dockerized deployment
* CI/CD pipeline using **GitHub Actions**
* Deployment on **AWS EC2** with self-hosted runner

---

## Tech Stack

* **Python 3.10**
* **Database:** MongoDB Atlas
* **Cloud:** AWS (S3, EC2, ECR, IAM)
* **MLOps:** MLflow, DVC (basics)
* **DevOps:** Docker, GitHub Actions

---

## Project Highlights

* Clean, component-based pipeline architecture
* Environment-variable driven configuration
* Model versioning and comparison before deployment
* CI/CD automation from GitHub to AWS EC2
* Designed to resemble real-world ML production workflows

---

## High-Level Workflow

1. Create project template and local package structure
2. Setup virtual environment and dependencies
3. Push dataset to MongoDB Atlas
4. Ingest data from MongoDB into pipeline
5. Validate data using schema
6. Transform data and train model
7. Evaluate model against existing version
8. Store approved model in AWS S3
9. Deploy application using Docker and CI/CD
10. Serve prediction and training routes on EC2

---

## Running the Project (Quick)

```bash
conda create -n vehicle python=3.10 -y
conda activate vehicle
pip install -r requirements.txt
```

Set required environment variables:

* `MONGODB_URL`
* `AWS_ACCESS_KEY_ID`
* `AWS_SECRET_ACCESS_KEY`
* `AWS_DEFAULT_REGION`

Run:

```bash
python app.py
```

---

## Deployment

* Docker image built and pushed to AWS ECR
* CI/CD triggered on GitHub push
* Application deployed on AWS EC2
* Accessible via EC2 public IP on port **5080**

---

## Why This Project Matters

This project demonstrates **how machine learning systems are engineered, deployed, and maintained in production**, covering data pipelines, cloud storage, CI/CD, and deployment — not just model accuracy.


