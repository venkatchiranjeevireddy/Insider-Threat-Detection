🔐 TL INSIGHT
Temporal Logic-Enhanced Spiking Graph Neural Network for Insider Threat Detection
📌 Project Overview

Insider threats are among the most dangerous cybersecurity risks because they originate from users who already have authorized access to systems. Their actions often look normal at first glance, making detection extremely difficult using traditional rule-based or machine learning systems.

TL INSIGHT introduces a neuro-symbolic security framework that intelligently combines graph learning, spiking neural computation, and symbolic reasoning to detect insider threats with high accuracy and explainability.

🎯 Key Goals

Identify hidden insider threats within normal user behavior

Capture temporal behavior patterns over time

Learn relationships between user activities

Handle extreme class imbalance in security datasets

Minimize false negatives, which are critical in cybersecurity

Provide interpretable and explainable results

🧠 Core Idea (What Makes It Special?)

TL INSIGHT is built on the idea that insider threats are not isolated events — they evolve over time, across related activities, and often follow logical patterns.

To address this, the system integrates:

🕸 Graph Neural Networks (GNNs) → model relationships

⚡ Spiking Neural Networks (SNNs) → model temporal behavior

📜 Symbolic Rules → inject human expertise

🎯 Focal Loss → focus learning on rare insider cases

📂 Dataset Used

CERT r5.2 Insider Threat Dataset

Realistic enterprise user activity logs

Highly imbalanced (very few insider threat cases)

🔖 Label Definition

Class 0 → Normal user activity

Classes 1–4 → Insider threat activity

For practical deployment, the task is converted into binary classification:

0 → Non-Threat

1 → Threat

🏗 System Architecture (Workflow)

1️⃣ Feature Engineering

Numerical behavior features

Domain-based symbolic rules

2️⃣ Data Standardization

Normalization for stable learning

3️⃣ Similarity Graph Construction

Nodes = user activity samples

Edges = cosine similarity above threshold

4️⃣ Spiking Graph Neural Network

GCN layers learn structural patterns

Spiking neurons capture temporal behavior

5️⃣ Threat Classification

Outputs threat probability

6️⃣ Threshold Optimization

Adjusts decision boundary to reduce false negatives

7️⃣ Evaluation & Reporting

Classification report

Confusion matrix

📜 Symbolic Rule Injection

To improve interpretability, TL INSIGHT integrates symbolic Boolean rules derived from cybersecurity knowledge, such as:

Unusual access timings

Suspicious file or device usage

Abnormal activity combinations

Each rule outputs 0 or 1, which is combined with numerical features.
This makes the system both data-driven and logic-aware.

⚡ Spiking Graph Neural Network (S-GNN)

Unlike traditional neural networks, spiking neurons process data over time, similar to biological brains.

Why this matters:

Captures slow-evolving insider attacks

Ignores short-term noise

Focuses on persistent suspicious behavior

The GNN captures who is related to whom, while the SNN captures when behavior becomes suspicious.

⚖ Handling Class Imbalance

Insider threat data is extremely skewed. TL INSIGHT addresses this using:

🎯 Focal Loss → focuses on hard-to-detect insider samples

⚖ Class weighting → penalizes missed threats

🔽 Majority class down-sampling → improves learning balance

🎚 Threshold Optimization

Instead of using a fixed decision threshold:

The threshold is tuned after training

Focus is on minimizing false negatives

This aligns with real-world security priorities

📊 Experimental Results

🚀 ROC-AUC: 96.5%

Strong improvement in insider threat recall

Significant reduction in false negatives

Stable training without overfitting

Balanced performance on reduced datasets

🌟 Key Advantages

✅ Temporal + relational + logical learning

✅ Explainable and interpretable predictions

✅ Robust to highly imbalanced data

✅ Suitable for real-world enterprise security

✅ Inspired by biological neural systems

🏢 Applications

Enterprise Insider Threat Detection

Security Operations Centers (SOC)

User Behavior Analytics (UBA)

Cyber Risk Monitoring Systems

🧾 Conclusion

TL INSIGHT presents a powerful and explainable insider threat detection framework by integrating symbolic logic, spiking neural computation, and graph deep learning. It overcomes key limitations of traditional ML and DL systems, making it well-suited for modern enterprise cybersecurity environments.

Future extensions may include real-time deployment, automated rule discovery, and expansion to other anomaly detection domains.
