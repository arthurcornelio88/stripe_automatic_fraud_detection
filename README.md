# Automatic Fraud Detection Project

This project provides a complete pipeline for fraud detection, from data engineering to model training and serving. It is composed of two main services, each in its own repository.

---

## 📂 Project Repositories

This project is split into two core repositories:

* ➡️ **[dataops_pipeline](https://github.com/arthurcornelio88/stripe_dataops_pipeline)**: Contains all code for the data engineering pipeline, including data ingestion, cleaning, and preparation (ETL), orchestrated by Airflow.

* ➡️ **[model_training](https://github.com/arthurcornelio88/stripe_model_training)**: Contains the notebooks and scripts for training, evaluating, and serving the classification model for fraud detection.

---

## 🚀 Getting Started (Development Environment)

To run this project locally, you need to containerize and run each service independently. This requires two separate terminal windows.

1.  **Clone both repositories** to your local machine:
    ```bash
    git clone git@github.com:arthurcornelio88/stripe_model_training.git
    git clone git@github.com:arthurcornelio88/stripe_dataops_pipeline.git 
    ```

2.  **Open two terminal windows.**

3.  In the **first terminal**, navigate to the `dataops_pipeline` directory and start its services using Docker Compose:
    ```bash
    cd dataops_pipeline
    docker-compose up --build
    ```

4.  In the **second terminal**, navigate to the `model_training` directory and start its services:
    ```bash
    cd model_training
    docker-compose up --build
    ```

Each service will now be running in its own isolated, containerized environment.

---

## ☁️ Production Deployment

For detailed instructions on how to deploy these services to a production environment (like GCP VMs), please refer to the specific documentation within each repository's `README.md` or `/docs` folder.