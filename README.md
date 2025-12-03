## 📘 Project Overview

This project is an **Agentic AI–powered Deal Detection and Price Estimation System** designed to track online product deals, estimate fair pricing using multiple AI models, and notify users automatically.

---
<img width="300" height="250" alt="ChatGPT Image Dec 3, 2025, 12_02_28 AM" src="https://github.com/user-attachments/assets/914e23e1-3946-480e-b32e-867e728fa0e4" />


## 🔍 Key Features

### **1. Scanner Agent (Web Deal Scraper)**
- Scrapes the latest product deals from online sources.
- Extracts product title, discounted price, and product URL.
- Runs automatically at configurable intervals (default: every 1 minute).

### **2. Ensemble Pricing Agent**
Generates highly accurate estimated prices using a hybrid AI+ML approach:
- **QLoRA-finetuned LLaMA model** (62.8% hit rate vs 28% baseline)
- **RAG-based price lookup** from curated Amazon metadata
- **Random Forest model**
- **Linear Regression model**

All models are merged to produce a stable, accurate final estimated price.

### **3. Notification Agent**
- Sends deal alerts to users via email or messaging service.
- Includes:
  - Estimated Price (AI + ML ensemble)
  - Discounted Price (scraped)
  - Product URL
- Ensures timely updates with structured, reliable messages.

### **4. Persistent Memory (JSON Storage)**
- Stores processed deals to avoid duplicates.
- Maintains context across runs.
- Ensures users are notified only about new deals.

---

## 🧠 AI & ML Components Used
- **QLoRA fine-tuning** on LLaMA
- **RAG (Retrieval-Augmented Generation)** using ChromaDB
- **Random Forest Regressor**
- **Linear Regression**
- **Structured Outputs** for robust agent-to-agent communication

---

## 🛠️ Tech Stack
- **Python**, **Hugging Face**, **QLoRA**, **Gradio**, **RAG**
- **ChromaDB** for vector search
- **Modal** for serverless execution
- **W&B** for experiment tracking
- **JSON-based persistent storage**

---

## 📈 Model Performance
Improved price prediction accuracy:
- **Finetuned LLaMA: 62.8% hits**
- **Baseline LLaMA: 28%**

Custom QLoRA training achieved **2× performance improvement** with stable training metrics.

---

