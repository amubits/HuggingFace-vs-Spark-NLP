# Big Data Analytics Project: Leveraging Hugging Face's Pre-Trained Models for Advanced Text Classification

This repository contains the resources and notebooks for our text classification project using both Spark NLP and Hugging Face's Transformers. This work is completed in partial fulfillment of the requirements for the Big Data Analytics course offered by the Master of Science in Business Analytics program at the Carlson School of Management, University of Minnesota.

## Project Overview

This project is designed to critically assess and compare the efficacy of Spark NLP 5.1.4 and Hugging Face's Transformers in applying and fine-tuning pre-trained BERT models for text classification tasks. By building and adjusting a BERT classification model using Spark NLP and contrasting it with Hugging Face’s DistilBERT base uncased model, the study aims to evaluate their performance based on accuracy, precision, recall, and computational efficiency metrics. This comparison will shed light on the adaptability of these models to specific datasets and tasks, focusing on their minimal training requirements and resource optimization, particularly in GPU utilization and data processing techniques like batching.
The project's primary objective is to offer insights into the suitability of Spark NLP and Hugging Face Transformers for various applications in business analytics, emphasizing their strengths and limitations in real-world settings. The findings will guide practitioners in selecting the most appropriate NLP tools for their specific needs, thereby underscoring the practical applications and customization potential of advanced pre-trained models in the rapidly evolving domain of NLP.

The aim of this project is twofold:
1. To leverage Spark NLP to classify SMS messages as spam or not spam using a pre-trained BERT model.
2. To fine-tune a DistilBERT model using Hugging Face's Transformers and MLflow for the same classification task.

## Repository Contents

- `Bertclassification_final.ipynb`: Jupyter notebook with Spark NLP code for text classification.
- `MLFlow_X_HuggingFace_Finetune_a_text_classification_mode.ipynb`: Jupyter notebook demonstrating fine-tuning of a DistilBERT model with MLflow integration.
- `README.md`: This file, serving as the project homepage and executive summary.

## Quick Links

- [Project Video](https://drive.google.com/file/d/1J5Gr5A80jjO_ORz4XbRHtPbNuIXpGcg6/view)
- [Dataset Source](https://archive.ics.uci.edu/ml/machine-learning-databases/00228/smsspamcollection.zip)
- [Additional Resources](https://www.databricks.com/blog/2023/02/06/getting-started-nlp-using-hugging-face-transformers-pipelines.html)
- [Additional Resources](https://www.techtarget.com/whatis/definition/Hugging-Face#:~:text=Hugging%20Face%20provides%20access%20to%20a%20vast%20community%2C%20continuously%20updated,Face's%20hosted%20models%20saves%20money)

## Getting Started

To reuse and run this project's code, please follow the setup instructions below.

### Prerequisites

- Apache Spark version 3.2.3
- Spark NLP version 5.1.4
- Hugging Face Transformers library
- MLflow
- An environment capable of running Jupyter notebooks

### Installation and Setup

1. Install the required libraries:
   - For Spark NLP: `pip install spark-nlp==5.1.4`
   - For Hugging Face Transformers: `pip install transformers datasets`
   - For MLflow: `pip install mlflow`
2. Download the SMS Spam Collection dataset and extract its contents.
3. Launch a Jupyter notebook server in an environment where the libraries are installed.
4. Open and run the notebooks: `Bertclassification_final.ipynb` and `MLFlow_X_HuggingFace_Finetune_a_text_classification_mode.ipynb`.

### Running the Notebook

Execute each cell in the Jupyter notebook in order. The main steps are:

- Initializing Spark NLP components
- Building and fitting the classification pipeline
- Evaluating model performance

The expected output is the accuracy of the SMS spam classification model.

### Notebooks Execution Guide

#### Bertclassification_final.ipynb

- Initialize Spark NLP components and create the pipeline.
- Fit the model to the training data and perform predictions.
- Evaluate the model's accuracy.

#### MLFlow_X_HuggingFace_Finetune_a_text_classification_mode.ipynb

- Convert Spark DataFrame to Hugging Face datasets.
- Tokenize and prepare the data for training.
- Fine-tune the DistilBERT model using Hugging Face's Trainer API.
- Log metrics and results to MLflow and wrap the model for direct spam classification.
