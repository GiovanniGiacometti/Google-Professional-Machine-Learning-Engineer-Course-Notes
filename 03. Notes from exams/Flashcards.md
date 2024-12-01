
Vertex AI Vizier is an independent service for optimizing complex models with many parameters while Hyperparameter tuning for custom training is a built‐in feature that uses Vertex AI Vizier for training jobs.

Random search, parallel computing, using a simple validation set instead of cross‐validation if you have a large dataset, and caching the results of computations are 4 ways to speed up hyperparameter tuning jobs

The TFX pipeline component Pusher deploys the model on a serving infrastructure and BulkInferrer performs batch processing on a model with unlabeled inference requests.

Instance types for GPUs -> A2 or N1

When you run a Kubeflow pipeline, the system launches one or more kubernets Pods corresponding to the steps (components) in your workflow (pipeline).

You cannot export BigQuery ML models into Vertex AI if you had used the TRANSFORM clause when creating the model.

Some of the advantages of using Vertex AI [[Managed datasets]] is managing datasets in a central location, integrated data labeling for unlabeled unstructured data, and automatically split between train, test and validation

NVIDIA_TESLA_A100 -> most powerful GPU in google cloud

Google Cloud Pipeline Components -> library that helps using prebuilt google components in [[Kubeflow]] Pipelines sdk

Tensorflow Serving -> host a trained model as an API endpoint. Handles model serving and version management

Frequently bought together -> increase revenue in Recommendations AI

Feature attribution: instance level, provides a score of how much each feature contributed to the model's prediction. 3 methods:
- sampled shapley 
- integrated gradients (mostly images, also tabular)
- xrai (only images)

What type of NoSQL databases in Google Cloud can be used to architect for use cases needing sub‐millisecond latency while serving or for online prediction -> Memorystore

Format preserving encryption -> preserves the format of information

Static Features -> value do not change in real time. Typically available in a data warehouse

AUC roc -> metric to use when you want scale invariance

Authenticated Encryption with Associated Data (AEAD) encryption functions -> You can encrypt individual table values in BigQuery