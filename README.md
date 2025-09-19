# 📞 ETL Pipeline for Telecom Call Detail Records (CDRs)

This repository contains an **SSIS-based ETL solution** for automating the ingestion, transformation, and storage of telecom call detail records (CDRs).  
The pipeline is designed to handle frequent raw data ingestion while ensuring **data quality, consistency, and auditability**.

---

## ✨ Key Features
- ⚡ **Automated Ingestion**: Detects and loads CSV files generated every 5 minutes.  
- 🧹 **Data Transformation & Validation**:  
  - Validates identifiers (IMSI, CELL, LAC)  
  - Enriches records with `subscriber_id` via reference table joins  
  - Extracts TAC and SNR, validates timestamp formats  
- 🚨 **Error Handling**: Captures, logs, and stores rejected records for later review.  
- 📂 **File Management**: Archives processed files to maintain integrity and prevent duplication.  

---

## 📊 Outcome
The pipeline ensures:  
- ✅ Clean, validated CDRs stored in a relational database  
- ⚙️ Reliable automation of workflows with SSIS  
- 📝 Full audit trail for rejected records  
- 📈 Scalable foundation for telecom data analysis and reporting  

---

## 🛠️ Tools & Technologies
- 🖥️ **SQL Server Integration Services (SSIS)** – ETL workflows  
- 🗄️ **SQL Server Management Studio (SSMS)** – database management  
- 📑 **CSV** – raw data input format  
- 🏗️ **SQL Server** – relational database for storing processed data  


---

## 🚀 Skills Demonstrated
- Data pipeline development  
- Data quality & validation techniques  
- Automated workflows with SSIS  
- Relational database integration in a telecom context  

---

