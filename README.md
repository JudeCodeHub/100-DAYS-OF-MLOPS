# 100 Days of MLOps Challenge

Welcome to my repository for the **100 Days of MLOps Challenge**! This hands-on initiative is designed to bridge the gap between machine learning development and production operations by applying traditional DevOps principles to the lifecycle of AI models. 

The core focus of this challenge is to build, deploy, monitor, and maintain machine learning models reliably at scale using production-grade architecture.

---

## 🗺️ Core Curriculum & Domains Covered

The training path spans across three progressive difficulty tiers (Basic, Intermediate, and Advanced) distributed over 12 primary MLOps domains:

* **Environment & Project Architecture:** Establishing reproducible workspaces, dependency management, and isolated environments.
* **Data & Pipeline Versioning:** Implementing immutable data tracking and reproducible multi-stage pipelines.
* **Experimentation & Lineage Tracking:** Logging model parameters, metrics, artifacts, and training runs.
* **Model Registry & Governance:** Managing model versions, transition stages (Staging/Production), and metadata.
* **Continuous Integration & Training (CI/CT):** Automated testing of ML code and automated model retraining hooks.
* **Model Serving & Deployment:** Constructing highly scalable, production-ready inference endpoints (Batch & Real-time).
* **Production Orchestration:** Workflow automation, scheduling, and pipeline dependency routing.
* **Cloud Infrastructure & Containers:** Microservices containerization and enterprise cluster orchestration.
* **Observability & Monitoring:** Production model evaluation, logging tracking, and system health checks.
* **Data & Concept Drift Detection:** Statistical monitoring of data distribution shifts over time.
* **Feedback Loops & Retraining:** Closed-loop monitoring triggers to automatically retrain decaying models.
* **Capstone Integration:** Combining all 12 domains into a single, comprehensive end-to-end production ecosystem.

---

## 🛠️ Tech Stack & Ecosystem

The implementation workflows utilize standard enterprise technologies to handle production workloads:

| Domain | Tools & Technologies Used |
| :--- | :--- |
| **Data Versioning** | DVC (Data Version Control) |
| **Experiment Tracking** | MLflow |
| **Model Serving** | FastAPI, BentoML |
| **Drift & Monitoring** | Evidently AI |
| **Orchestration** | Prefect, Argo Workflows |
| **Infrastructure** | Kubernetes, Docker |