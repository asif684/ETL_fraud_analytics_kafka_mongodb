# 🕵️‍♂️ Fraud Analytics Big Data ETL Project

## 📘 Project Overview
This project demonstrates a **Fraud Analytics ETL (Extract, Transform, Load)** pipeline that detects potential fraudulent transactions in real-time using **Confluent Kafka**, **Databricks**, and **MongoDB**.  
The ETL pipeline streams transaction data, applies fraud detection logic, stores results, and sends email alerts for suspicious transactions.

---

## 🧩 Architecture Overview

### 🔄 ETL Workflow
![image alt](https://github.com/asif684/ETL_fraud_analytics_kafka_mongodb/blob/2e5b6ca1d9e909a202292c71ccd91070924ba28a/Screenshot%202025-10-18%20113835.png)

### Pipeline Stages:
1. **EXTRACT**
   - Producer sends data to **Confluent Kafka** topic.
2. **TRANSFORM**
   - Databricks consumes data and applies fraud detection logic.
3. **LOAD**
   - MongoDB stores results, triggers alerts, and sends fraud emails.

---

## ⚙️ Technologies Used

| Component | Technology | Description |
|------------|-------------|--------------|
| **Streaming Platform** | Confluent Kafka | Real-time data streaming |
| **Data Processing** | Databricks | Transforming and classifying transactions |
| **Database** | MongoDB | Storing fraud/non-fraud records |
| **Notification Service** | Python SMTP | Sending fraud alert emails |
| **Language** | Python | For all scripts |

---

## 🧠 ETL Pipeline Flow
```bash
Producer → Kafka Topic → Databricks Consumer → Fraud Logic → MongoDB → Trigger → Email Alert
