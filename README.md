TL INSIGHT

Temporal Logic-Enhanced Spiking Graph Neural Network for Insider Threat Detection

Project Overview

Insider threats are one of the most dangerous cybersecurity risks because they originate from users who already have authorized access to organizational systems. Traditional security and machine learning systems struggle to detect insider threats due to class imbalance, lack of interpretability, and inability to model long-term behavior patterns.

TL INSIGHT is a neuro-symbolic insider threat detection framework that combines:

Graph Neural Networks (GNNs)

Spiking Neural Networks (SNNs)

Symbolic rule-based reasoning

Focal Loss for imbalanced data handling

The system detects suspicious insider behavior with high accuracy while maintaining explainability and temporal awareness.

Key Objectives

Detect insider threats hidden within normal user behavior

Capture temporal, relational, and logical patterns

Handle extreme class imbalance in cybersecurity datasets

Reduce false negatives, which are critical in threat detection

Provide interpretable and explainable predictions

Dataset Used

CERT r5.2 Insider Threat Dataset

Realistic enterprise user behavior logs

Highly imbalanced with very few insider threat cases

Label Definition

Class 0 → Normal User Activity

Classes 1–4 → Insider Threat Activity

For practical detection, the problem is converted into binary classification:

0 → Non-Threat

1 → Threat

System Architecture

The TL INSIGHT pipeline consists of the following stages:

Feature Engineering

Raw numerical features from logs

Symbolic Boolean rules derived from domain knowledge

Data Standardization

Features normalized using standard scaling

Graph Construction

Cosine similarity used to dynamically build graphs

Nodes represent user activity samples

Edges created when similarity exceeds a threshold

Spiking Graph Neural Network

Graph Convolutional Networks capture relationships

Leaky Integrate-and-Fire neurons model temporal behavior

Classification Layer

Outputs threat probability

Threshold Optimization

Decision threshold tuned to reduce false negatives

Evaluation

Classification report and confusion matrix

Symbolic Rule Integration

Symbolic rules encode expert knowledge such as:

Unusual login times

Suspicious file access patterns

Removable device usage

High-risk activity sequences

Each rule outputs a binary value (0 or 1).
These symbolic features are combined with numerical features, making the model both data-driven and knowledge-driven.

Spiking Graph Neural Network (S-GNN)

Uses Graph Convolutional Layers for relational learning

Uses Spiking Neurons for temporal learning

Mimics biological neural behavior

Focuses on persistent abnormal activity instead of short-term noise

This allows the system to detect slow-evolving insider attacks.

Handling Class Imbalance

Insider threat data is highly skewed toward normal behavior.
TL INSIGHT addresses this using:

Focal Loss

Focuses training on difficult minority class samples

Class Weighting

Penalizes misclassification of insider threats

Majority Class Down-Sampling

Only 10% of normal data retained in experiments

Threshold Tuning Strategy

Instead of using a fixed probability threshold:

The classification threshold is tuned after training

Objective is to minimize false negatives

This is critical because missing a threat is more dangerous than a false alarm

Experimental Results

ROC-AUC achieved: 96.5%

Strong improvement in insider threat recall

Reduced false negatives compared to baseline models

Stable training with no overfitting

Balanced precision and recall in reduced dataset

Advantages of TL INSIGHT

Combines temporal, relational, and logical reasoning

Interpretable due to symbolic rules

Robust to extreme class imbalance

Suitable for real-world enterprise security systems

Biologically inspired and explainable AI approach

Applications

Enterprise Insider Threat Detection

Security Operations Centers (SOC)

Continuous User Behavior Monitoring

Cyber Risk Management Systems

Conclusion

TL INSIGHT presents a powerful and interpretable insider threat detection framework by integrating symbolic reasoning, spiking neural computation, and graph deep learning. It overcomes major limitations of traditional machine learning and deep learning models, making it well-suited for real-world cybersecurity environments.