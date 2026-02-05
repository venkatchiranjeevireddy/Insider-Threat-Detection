# 🔐 TL INSIGHT  
### Temporal Logic-Enhanced Spiking Graph Neural Network for Insider Threat Detection

---

## 📖 Overview

Insider threats are among the most dangerous cybersecurity risks because they originate from users who already have authorized access to organizational systems. Their actions often appear normal, making detection extremely difficult using traditional rule-based or machine learning approaches.

**TL INSIGHT** introduces a **neuro-symbolic insider threat detection framework** that combines **graph learning**, **spiking neural networks**, and **symbolic reasoning** to detect insider threats with high accuracy and improved explainability.

---

## 🎯 Key Objectives

- Identify hidden insider threats within normal user behavior  
- Capture temporal behavior patterns over time  
- Learn relationships between user activities  
- Handle extreme class imbalance in insider threat datasets  
- Reduce false negatives, which are critical in cybersecurity  

---

## 🧠 Core Idea

Insider threats are rarely single events. They evolve over time, involve multiple actions, and follow logical patterns.

TL INSIGHT addresses this by integrating:

- 🕸 **Graph Neural Networks (GNNs)** to model relationships  
- ⚡ **Spiking Neural Networks (SNNs)** to model temporal behavior  
- 📜 **Symbolic Rules** to inject domain knowledge  
- 🎯 **Focal Loss** to focus learning on rare insider threats  

---

## 📂 Dataset

- **CERT r5.2 Insider Threat Dataset**
- Enterprise-scale user activity logs
- Highly imbalanced with very few insider threat samples

### Label Mapping

- Class 0 → Normal Activity  
- Classes 1–4 → Insider Threat  

Converted into binary classification:

- `0` → Non-Threat  
- `1` → Threat  

---

## 🏗 System Architecture

The TL INSIGHT pipeline follows these steps:

1. **Feature Engineering**
   - Numerical behavior features  
   - Symbolic Boolean rules  

2. **Data Standardization**
   - Feature normalization  

3. **Similarity Graph Construction**
   - Nodes represent activity samples  
   - Edges created using cosine similarity  

4. **Spiking Graph Neural Network**
   - GCN layers for relational learning  
   - Spiking neurons for temporal modeling  

5. **Threat Classification**
   - Outputs threat probability  

6. **Threshold Optimization**
   - Adjusted to minimize false negatives  

7. **Evaluation**
   - Classification report  
   - Confusion matrix  

---

## 📜 Symbolic Rule Integration

Symbolic rules represent expert cybersecurity knowledge such as:

- Unusual access times  
- Suspicious file or device usage  
- Abnormal activity sequences  

Each rule outputs a binary value (0 or 1), which is combined with numerical features.  
This improves both **performance** and **interpretability**.

---

## ⚡ Spiking Graph Neural Network (S-GNN)

- Spiking neurons process information over time  
- Focus on persistent suspicious behavior  
- Ignore short-term noise  
- Inspired by biological neural systems  

The GNN captures **relationships**, while the SNN captures **temporal evolution** of insider behavior.

---

## ⚖ Handling Class Imbalance

TL INSIGHT addresses imbalance using:

- **Focal Loss** to focus on hard-to-detect samples  
- **Class weighting** to penalize missed threats  
- **Majority class down-sampling** for balanced learning  

---

## 🎚 Threshold Optimization

Instead of using a fixed probability threshold:

- Threshold is tuned after training  
- Focus is on reducing false negatives  
- Aligns with real-world security requirements  

---

## 📊 Results Summary

- ROC-AUC: **96.5%**  
- Improved insider threat recall  
- Reduced false negatives  
- Stable training without overfitting  
- Strong performance on reduced datasets  

---

## 🌟 Key Advantages

- Combines temporal, relational, and logical reasoning  
- Explainable and interpretable predictions  
- Robust to highly imbalanced data  
- Suitable for enterprise cybersecurity systems  

---

## 🏢 Applications

- Insider Threat Detection Systems  
- Security Operations Centers (SOC)  
- User Behavior Analytics  
- Cyber Risk Monitoring  

---

## 🧾 Conclusion

TL INSIGHT presents a hybrid neuro-symbolic framework that integrates symbolic reasoning, spiking neural computation, and graph deep learning to effectively detect insider threats. The approach overcomes major limitations of traditional ML and DL models, making it suitable for modern enterprise cybersecurity environments.

---

## 🔑 Keywords

Insider Threat Detection, Spiking Neural Networks, Graph Neural Networks, Neuro-Symbolic AI, Focal Loss, Cybersecurity
