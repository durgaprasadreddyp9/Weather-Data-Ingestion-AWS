# ☁️ AWS Real-Time Weather Data Pipeline

## 📌 Overview
This project implements an **end-to-end real-time data pipeline** on **AWS** to **fetch, process, store, and analyze weather data** from an external API. The pipeline is **serverless**, leveraging **AWS Lambda, DynamoDB, S3, and Snowflake** for efficient data ingestion, transformation, and querying.

### 🔹 **Key Features:**
✅ **Real-time Weather Data** – Fetches live weather data from an API every hour.  
✅ **Serverless Architecture** – AWS Lambda automates data processing.  
✅ **DynamoDB Storage** – Stores structured weather data for fast retrieval.  
✅ **S3 Data Lake** – Streams processed data to Amazon S3 for long-term storage.  
✅ **Snowflake Integration** – Loads data into Snowflake for analytics.  
✅ **Fully Automated** – The pipeline is scheduled to run **every hour**.  

---


## 🔄 Workflow

### **1️⃣ Fetch Real-Time Weather Data**
- AWS Lambda function calls an **external weather API** every hour.
- The API response is **parsed and structured**.

### **2️⃣ Store Data in DynamoDB**
- The processed data is **inserted into DynamoDB**, allowing quick lookups.

### **3️⃣ Stream Data to S3**
- Another **Lambda function** streams data from DynamoDB to an **S3 bucket** for long-term storage.

### **4️⃣ Load Data into Snowflake**
- **AWS Lambda** triggers a **Snowflake COPY INTO** command.
- Data is **transformed** and loaded into **Snowflake tables** for analytics.

### **5️⃣ Query & Analyze Data in Snowflake**
- Run **SQL queries** on Snowflake to analyze **weather patterns, temperature trends, and forecasts**.



