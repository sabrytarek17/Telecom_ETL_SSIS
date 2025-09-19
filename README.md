# 📡 Telecom ETL SSIS Project

This ETL project was developed using **SQL Server Integration Services (SSIS)** for a telecom company.  
The goal is to **extract transactional data from CSV files**, apply business transformation rules, and **load clean records into a SQL Server database** while isolating erroneous data for review.

---

## 🎯 Project Overview
The telecom company generates a CSV file every 5 minutes containing customer transaction data.  
The SSIS package performs the following operations:

- 🔄 Iterates over incoming files using a **Foreach Loop Container**  
- 📂 Extracts data from flat files via **Flat File Source**  
- 🧹 Applies transformation logic using **Derived Columns, Lookups, and Conditional Splits**  
- ✅ Loads valid records into the main transaction table  
- ❌ Redirects invalid records to error tables with **source tracking**  

---

## 🧰 Tools & Technologies
- 💻 **Microsoft Visual Studio (SSDT)** – SSIS package development  
- 🗄️ **SQL Server Management Studio (SSMS)** – Database management  
- ⚙️ **SSIS Components** – Foreach Loop, Data Flow Task, File System Task, OLE DB Destination, etc.  
- 📑 **File Handling** – Source files from `C:\SSIS_Source_Files`, processed files moved to `C:\Processed_Files`  

---


## 🧪 Transformation Rules
<img width="905" height="585" alt="Image" src="https://github.com/user-attachments/assets/ae4f504a-6b6d-40e8-a624-ff5df159d4bc" />

---

## 🗃️ Database & Tables
Database used: **SSIS_Telecom_DB**

- 🔍 **[dbo].[dim_imsi_reference]** – Reference table for IMSI validation  
- 📄 **[dbo].[error_source_output]** – Tracks error source and original file name  
- ✅ **[dbo].[telecom_transaction]** – Stores clean, validated records  
- ❌ **[dbo].[error_transaction]** – Stores rejected rows based on transformation rules  

---

## 🖼️ Data Flow Screenshots

<img width="1016" height="437" alt="Image" src="https://github.com/user-attachments/assets/ffcc3efc-9bf0-4070-b433-774fc635b14a" />

<img width="972" height="387" alt="Image" src="https://github.com/user-attachments/assets/ebff865f-edf3-4adb-91b9-160b8cf0c6db" />

---

## ⚙️ Requirements
- Visual Studio with **SSDT** installed  
- SQL Server 2019 or later  
- Properly formatted CSV files from the telecom system  
- Execution permissions for SSIS packages and database access  

---

## 🚀 Execution Steps
1. Open the SSIS project in **Visual Studio**  
2. Configure connection settings as per your environment  
3. Run the package via **Data Flow** or **Foreach Loop**  
4. Verify data in `telecom_transaction` and `error_transaction` tables  
5. Review `error_source_output` for file-level error tracking  

---

## 📊 Outcome
The pipeline ensures:  
- ✅ Clean, validated transactions stored in a relational database  
- 🚨 Full logging & audit trail for rejected records  
- 📈 Scalable design for telecom data analysis & reporting  

