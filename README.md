# 📦 What is Azure Data Factory?

Azure Data Factory (ADF) is a **cloud-based data integration service** that allows you to migrate data from **source to destination** using:

- 🔄 **ETL** (Extract, Transform, Load)  
- 🔁 **ELT** (Extract, Load, Transform)  

---

## 💡 Key Concepts

- 🔌 Uses **connectors** to link different data sources and destinations  
- 📊 Supports both **structured** and **unstructured** data  



### 📤 Common Destinations:
- 🪣 Azure Blob Storage  
- 🏞️ Azure Data Lake Gen2  
- ☁️ AWS S3  

---

# ⚙️ Understanding the ETL Process in ADF

## 1️⃣ Extract
- 📦 Pulls data from various sources  
- 🔌 Uses **built-in connectors** based on data types (e.g., SQL, files, APIs)  

## 2️⃣ Load
- 🚛 Moves extracted data to a destination  
- Can be:  
  - 🔄 After transformation (**ETL**)  
  - 🧊 Before transformation (**ELT**)  

## 3️⃣ Transform
- 🧬 Modifies or reshapes the data  
- 🔧 Performed using **Data Flows** in ADF  

---

# 🔀 What are Data Flows?

**Data Flows** in ADF are **graphical tools** for designing transformation logic **without writing code**.

### 📝 Key Points:
- ⚡ Built on **Apache Spark clusters** (managed internally by ADF)  
- 🖱️ Uses **drag-and-drop GUI**  
- 📈 Scales automatically to handle large data volumes  

---

# ✅ Types of ETL/E Activities in Data Factory

## 🚚 1. Data Movement Activities
- Moves data between sources and sinks:  
  - 🔄 **Data Lake ⟶ Data Lake**  
  - 🌐 **API/HTTP ⟶ Data Lake**  

> 💡 Also known as **Copy Activity** in ADF

---

## 🔧 2. Data Transformation Activities
- Performed via **Data Flows**:  
  - 🛠️ Use **Expression Builder**  
  - 🧪 Apply transformations: filter, join, aggregate, derive columns, etc.

---

## 🧠 3. Control Activities
Used to **orchestrate** logic and control the pipeline flow:

- 🧾 **Get Metadata Activity**  
- 🧮 **Set Variable Activity**  
  - 🪪 Pipeline-level and return variables  
- 🔀 **If Condition Activity**  
- 🔁 **ForEach Activity**  
- 📂 **Execute Pipeline Activity**  

> 🧩 Useful for loops, branching, and modular design

---

## ⏰ 4. Triggering Activities / Events
- 🧲 **Storage Event Trigger**  
  - 🚨 Auto-trigger pipelines when a file is added or modified  
  - ⚙️ Enable/disable based on file type or path  

---

## 🧹 5. Cleanup or Utility Activities
- 🗑️ **Delete Activity**  
  - Cleans up temporary
  - Processed files after execution  

---
### 📥 Common Sources:
- 🗄️ SQL Database  
- 📁 CSV Files  
- 🌐 REST APIs  
