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

### 1. Clone the Repository
This will pull the full project structure including:
- dbt models
- Airflow DAGs
- Dockerfile
- Requirements
- Tests and Macros
- Documentation files
From here, you can proceed to build the Docker container and launch the pipeline.

### 2. Build Docker Environment
- Create a Dockerfile (This file defines everything needed to build a consistent environment)
- Create a requirements.txt file to install necessary packages
- Build the Docker Image from your project root
- Run the Container

### 3. Snowflake Setup
- Create warehouse, role, schema, and user
- Grant appropriate privileges

### 4. Configure Airflow Connection
In Airflow UI:
Go to Admin > Connections
Add a new Snowflake connection:
Conn ID: snowflake_conn
Use JSON in the “Extra” field:

### 5. Run dbt Models & Tests
- Build staging, intermediate, and fact models
- Materialize them as views or tables (as defined in your dbt_project.yml and dbt_profile.yml)
- Use dependency-aware order via ref() calls
##### Tests:
- Generic tests (e.g., unique, not_null, relationships, accepted_values)
- Custom tests (e.g., future-dated orders, discount sanity)

### 6. Generate and View dbt Docs
- dbt docs generate
- dbt docs serve

### 7. DAG Visualization in Airflow
- The DAG dynamically reflects the dbt project structure. Each dbt model becomes an individual task node, ordered according to the ref() dependencies.
- Schedule & Retry
-- Schedule Interval: @daily
-- Retries: Handled automatically by Airflow for failed models
-- Logs: Available per task (great for debugging broken transformations or tests)

### Features
- Clean separation of staging, intermediate, and fact models
- Built-in dbt tests for accuracy and data quality
- Reusable macros (like discounted_amount)
- Custom singular tests (like future dates or null revenue)
- Airflow DAG to schedule and orchestrate everything daily
- Modular, extensible, and ready for production pipelines

![Raw Data](https://github.com/user-attachments/assets/3eb69ede-7926-4ae6-bed2-1ae68462dc29)


## 👋 Author
#### Siddhant Mene
📊 Product & Data Enthusiast
📫 siddhant.mene@utdallas.edu
🌐 LinkedIn: https://www.linkedin.com/in/siddhantmene/

