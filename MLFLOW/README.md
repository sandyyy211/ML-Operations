# MLflow Model Training and Tracking

This repository demonstrates the implementation of MLflow for tracking and managing machine learning experiments, with a focus on text classification using the DistilBERT model.

## Project Overview

This project showcases:
- Integration of MLflow for experiment tracking
- Text classification using DistilBERT
- Model training and evaluation
- Model versioning and management
- AWS S3 integration for artifact storage

## Prerequisites

- Python 3.8+
- AWS CLI configured with appropriate credentials
- MLflow server running (default: http://localhost:5000)

## Installation

1. Clone the repository:
```bash
git clone <repository-url>
cd mlflow
```

2. Install required packages:
```bash
pip install mlflow==2.7.1 datasets==2.14.6 transformers==4.43.3 scikit-learn==1.3.0 tqdm==4.65.0 boto3 awscli
```

## Required Dependencies

- mlflow==2.7.1
- datasets==2.14.6
- transformers==4.43.3
- scikit-learn==1.3.0
- tqdm==4.65.0
- boto3
- awscli

## Project Structure

```
mlflow/
├── notebooks/
│   ├── Mlflow for Tracking Model Training .ipynb
│   ├── Mlflow AWS Setup and Basic Usage .ipynb
│   └── mlflow-inferenceipynb.ipynb
├── MLflow on AWS Setup.txt
└── README.md
```

## Usage

### 1. AWS Setup and Basic Usage

The `Mlflow AWS Setup and Basic Usage .ipynb` notebook covers:
- AWS configuration for MLflow
- Basic MLflow setup and usage
- Model versioning and management
- Model lineage tracking


### 2. Model Training and Tracking

The `Mlflow for Tracking Model Training .ipynb` notebook demonstrates:
- Setting up MLflow tracking
- Training a DistilBERT model for text classification
- Logging parameters, metrics, and artifacts
- Model evaluation and performance tracking

### 3. Model Inference

The `mlflow-inferenceipynb.ipynb` notebook shows:
- Model deployment
- REST API endpoint creation
- Model inference
- Performance monitoring

## Configuration

1. Set up MLflow tracking URI:
```python
mlflow.set_tracking_uri("http://your-mlflow-server:5000/")
```

2. Configure AWS credentials:
```bash
aws configure
```

## Model Training Parameters

- Model: distilbert-base-cased
- Learning Rate: 5e-5
- Batch Size: 16
- Number of Epochs: 1
- Dataset: AG News
- Max Sequence Length: 128

