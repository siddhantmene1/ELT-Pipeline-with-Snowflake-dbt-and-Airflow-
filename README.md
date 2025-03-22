# 🚀 ELT Pipeline with dbt + Snowflake + Airflow + Docker

A production-ready ELT (Extract, Load, Transform) pipeline built using modern data engineering tools.

---

## 🧰 Stack Used

| Tool         | Purpose                                             |
|--------------|-----------------------------------------------------|
| **Snowflake**| Cloud Data Warehouse for scalable storage & compute |
| **dbt**      | SQL-based data transformation + testing framework   |
| **Apache Airflow** | Workflow orchestration & automation         |
| **Docker**   | Containerization to ensure consistency              |

---

## ⚙️ Setup Instructions

### 🧱 1. Clone the Repository
### 🐳 2. Build Docker Environment
### ❄️ 3. Snowflake Setup
Create warehouse, role, schema, and user
Grant appropriate privileges
### 💻 4. Configure Airflow Connection
In Airflow UI:
Go to Admin > Connections
Add a new Snowflake connection:
Conn ID: snowflake_conn
Use JSON in the “Extra” field:
### 🧪 5. Run dbt Models & Tests
### 📄 6. Generate and View dbt Docs
### 📊 7. DAG Visualization in Airflow
### 🧠 Features
- Clean separation of staging, intermediate, and fact models
- Built-in dbt tests for accuracy and data quality
- Reusable macros (like discounted_amount)
- Custom singular tests (like future dates or null revenue)
- Airflow DAG to schedule and orchestrate everything daily
- Modular, extensible, and ready for production pipelines

![Raw Data](https://github.com/user-attachments/assets/3eb69ede-7926-4ae6-bed2-1ae68462dc29)


## 👋 Author
#### Siddhant Mene
🎓 Grad Student @ UT Dallas • 📊 Product & Data Enthusiast
📫 siddhant.mene@utdallas.edu
🌐 LinkedIn: https://www.linkedin.com/in/siddhantmene/

