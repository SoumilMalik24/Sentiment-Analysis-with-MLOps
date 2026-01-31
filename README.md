# Sentiment Analysis with MLOps

### Production-Grade NLP System with End-to-End Machine Learning Lifecycle

---

## 📘 Overview

**Sentiment-Analysis-with-MLOps** is a production-oriented Machine Learning Operations (MLOps) project that demonstrates the complete lifecycle of a Natural Language Processing (NLP) system — from raw data ingestion to scalable model deployment and monitoring.

This project is designed to mirror **real-world ML engineering workflows**, emphasizing:

* Reproducibility
* Experiment traceability
* Model governance
* Automation and deployment readiness

The system performs **sentiment classification** on textual data (such as customer reviews, social media posts, or feedback messages) into:

* ✅ Positive
* ❌ Negative


Modern Transformer-based architectures (e.g., BERT-family models) are leveraged alongside industry-standard MLOps tooling.

---

## 🎯 Objectives

The primary objectives of this project are:

* Build a **robust NLP training pipeline**
* Implement **experiment tracking and model versioning**
* Enable **data and artifact reproducibility**
* Design a **modular, scalable codebase**
* Deploy models through a **production-ready inference API**
* Simulate **real MLOps workflows used in industry**

This project is suitable as a reference architecture for **ML Engineer, MLOps Engineer, and Applied NLP roles**.

---

## ✨ Core Capabilities

### 🔁 End-to-End ML Pipeline

* Automated pipeline covering:

  * Data ingestion
  * Text preprocessing & tokenization
  * Model training
  * Evaluation
  * Artifact generation

### 📦 Data & Artifact Versioning (DVC)

* Dataset version control
* Reproducible experiments
* Pipeline dependency tracking
* Remote storage compatibility (S3 / GDrive / local)

### 📊 Experiment Tracking (MLflow)

* Parameter logging
* Metric tracking
* Model comparison
* Run history visualization
* Model Registry integration

### 🧠 Transformer-Based Modeling

* Pretrained Hugging Face models
* Fine-tuning using PyTorch
* Configurable hyperparameters
* Scalable training structure

### 🚀 Model Serving

* High-performance REST API using **FastAPI**
* Real-time inference support
* Interactive Swagger documentation

### 🐳 Containerized Deployment

* Dockerized environment
* Consistent runtime across systems
* Deployment-ready architecture

### 🔄 CI/CD Ready Design

* GitHub Actions compatible
* Automated testing & validation support
* Reproducible deployment pipeline

---

## 🧰 Technology Stack

### Programming & Core Libraries

* **Python**
* **PyTorch**
* **Hugging Face Transformers**
* **Pandas, NumPy**

### MLOps & Infrastructure

* **DVC** — Data & pipeline versioning
* **MLflow** — Experiment tracking & model registry
* **Docker** — Environment containerization
* **GitHub Actions** — CI/CD automation

### Deployment

* **FastAPI**
* **Uvicorn**

---

## 🗂️ Project Architecture

```bash
Sentiment-Analysis-with-MLOps/
│
├── .github/workflows/        # CI/CD pipelines
│
├── data/                     # DVC-tracked datasets
│   ├── raw/                  # Raw immutable data
│   └── processed/            # Cleaned & tokenized data
│
├── models/                   # Trained model artifacts
│
├── notebooks/                # Research & experimentation
│
├── src/
│   ├── components/           # Core ML modules
│   │   ├── data_ingestion.py
│   │   ├── data_transformation.py
│   │   ├── model_trainer.py
│   │   └── model_evaluation.py
│
│   ├── pipeline/             # Orchestrated pipelines
│   │   ├── training_pipeline.py
│   │   └── prediction_pipeline.py
│
│   ├── utils/                # Logging, helpers, constants
│   └── app.py                # FastAPI inference service
│
├── dvc.yaml                  # Pipeline definition
├── params.yaml               # Config-driven training
├── metrics.json              # Evaluation results
├── Dockerfile                # Container specification
├── requirements.txt          # Dependencies
├── .gitignore
├── .dvcignore
└── README.md
```

---

## ⚙️ Setup & Installation

### Prerequisites

* Python ≥ 3.8
* Git
* Docker (optional but recommended)

---

### 1️⃣ Clone the Repository

```bash
git clone https://github.com/SoumilMalik24/Sentiment-Analysis-with-MLOps.git
cd Sentiment-Analysis-with-MLOps
```

---

### 2️⃣ Create Virtual Environment

```bash
conda create -n sentiment-mlops python=3.9 -y
conda activate sentiment-mlops
```

---

### 3️⃣ Install Dependencies

```bash
pip install -r requirements.txt
```

---

### 4️⃣ Pull Versioned Data

```bash
dvc pull
```

This restores datasets and trained artifacts from the configured remote storage.

---

## 🧪 Model Training

Run the complete training pipeline:

```bash
python src/pipeline/training_pipeline.py
```

Or reproduce the full pipeline via DVC:

```bash
dvc repro
```

DVC ensures:

* Deterministic runs
* Dependency tracking
* Automatic stage execution

---

## 📈 Experiment Tracking with MLflow

Launch the MLflow UI:

```bash
mlflow ui
```

Access at:

```
http://localhost:5000
```

Track:

* Hyperparameters
* Metrics
* Model artifacts
* Run comparisons

---

## 🌐 Inference API

Start the FastAPI service:

```bash
uvicorn src.app:app --host 0.0.0.0 --port 8000
```

### API Documentation

```
http://localhost:8000/docs
```

Features:

* Real-time predictions
* JSON-based input/output
* Interactive Swagger UI

---

## 🐳 Docker Deployment

### Build Image

```bash
docker build -t sentiment-mlops .
```

### Run Container

```bash
docker run -p 8000:8000 sentiment-mlops
```

The service becomes accessible at:

```
http://localhost:8000
```

---

## 🔧 Configuration Management (`params.yaml`)

All training parameters are centrally managed:

```yaml
base:
  project: sentiment-analysis
  random_state: 42

model:
  name: distilbert-base-uncased
  learning_rate: 2e-5
  batch_size: 16
  epochs: 3
```

This enables:

* Configuration-driven experimentation
* No hardcoded parameters
* Clean hyperparameter tuning

---

## 📌 Future Enhancements

* Model monitoring & drift detection
* A/B testing using MLflow Registry
* Kubernetes deployment
* Prometheus + Grafana monitoring
* Feature store integration
* Automated retraining triggers

---

## 🤝 Contribution Guidelines

Contributions are welcome.

1. Fork the repository
2. Create a feature branch
3. Commit changes
4. Push to your fork
5. Open a Pull Request

All contributions should follow clean coding and modular design principles.

---

## 📄 License

Licensed under the **MIT License**.

---

## 👤 Author

**Soumil Malik**
Machine Learning | Deep Learning | MLOps

* GitHub: [https://github.com/SoumilMalik24](https://github.com/SoumilMalik24)
* Kaggle: [https://www.kaggle.com/soumilmalik](https://www.kaggle.com/soumilmalik)
* Hugging Face: [https://huggingface.co/Soumil24](https://huggingface.co/Soumil24)

---

### ⭐ If this repository helped you, consider giving it a star!

---


