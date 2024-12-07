
# 🌟 **ELT Pipeline with Snowflake, DBT, and Airflow** 🌟

This project demonstrates how to build an ELT (Extract, Load, Transform) pipeline using cutting-edge tools such as **Snowflake**, **DBT**, and **Airflow**. By leveraging these technologies, we efficiently load and transform data to create robust, scalable data models for business insights.

---

## 🚀 **Project Overview**

In this tutorial, you will:

1. Extract data from the **Snowflake TPCH dataset**.
2. Load raw data into a **staging schema**.
3. Transform data using **DBT Core** to create:
   - **Fact tables**
   - **Data marts**
   - Business-ready models
4. Orchestrate the entire workflow using **Airflow**.

---

## 🔧 **Tech Stack**

- **Snowflake**: Data warehouse for scalable and performant data storage.
- **DBT (Data Build Tool)**: For data transformations and modeling.
- **Airflow**: Workflow orchestration and scheduling.

---

## 🛠️ **Setup Instructions**

### 1️⃣ Prerequisites
- A Snowflake account (free tier works fine).
- Python installed on your system.
- DBT Core installed (`pip install dbt-core`).
- A virtual environment set up for isolation.

### 2️⃣ Snowflake Configuration
1. Create a **Warehouse**, **Database**, and **Schema**:
   ```sql
   -- Use your Snowflake console
   CREATE WAREHOUSE dbt_warehouse WITH WAREHOUSE_SIZE='SMALL';
   CREATE DATABASE dbt_database;
   CREATE SCHEMA dbt_schema;
   CREATE ROLE dbt_role;
   GRANT USAGE ON WAREHOUSE dbt_warehouse TO ROLE dbt_role;
   GRANT ALL ON DATABASE dbt_database TO ROLE dbt_role;
   ```

2. Assign the role to your user:
   ```sql
   GRANT ROLE dbt_role TO USER your_user_name;
   ```

### 3️⃣ Initialize Your DBT Project
- Create a new project:
  ```bash
  dbt init your_project_name
  ```
- Configure it with your Snowflake credentials.

---

## 📁 **Project Structure**

```plaintext
📦 your_project_name
├── 📂 models/
│   ├── 📂 staging/
│   ├── 📂 marts/
├── 📂 macros/
├── 📂 tests/
├── 📂 seeds/
└── dbt_project.yml
```

### Key Directories:
- **`models/`**: Contains SQL models for staging and marts.
- **`macros/`**: Reusable SQL functions.
- **`tests/`**: Includes schema and data integrity tests.
- **`seeds/`**: Static reference datasets.

---

## 🛠️ **Key Features**

- **Fact Tables**: Aggregated data for numerical analysis.
- **Dimensional Models**: Pre-processed and optimized for BI tools.
- **RBAC (Role-Based Access Control)**: Ensures data security in Snowflake.
- **Incremental Models**: Efficiently process new or updated data.

---

## 📚 **How to Run the Pipeline**

1. **Run Staging Models**:
   ```bash
   dbt run --select staging
   ```

2. **Run Fact and Mart Models**:
   ```bash
   dbt run --select marts
   ```

3. **Run Tests**:
   ```bash
   dbt test
   ```

4. **Orchestrate with Airflow**:
   - Configure Airflow DAGs for end-to-end pipeline management.

---

## 🧪 **Learning Goals**

- Understand the **ELT** paradigm and how it differs from **ETL**.
- Learn to model data using **dimensional modeling techniques**.
- Set up and manage Snowflake environments.
- Write reusable macros and run tests in DBT.

---

## 📊 **Business Use Case**

- Build a sales dashboard using the TPCH dataset.
- Generate insights from:
  - **Order trends**.
  - **Customer behavior**.
  - **Revenue forecasting**.

---

## 🛡️ **Best Practices**

- Use staging models for one-to-one mappings with source tables.
- Separate transformations into layers (e.g., staging → marts).
- Test relationships and data integrity in your pipelines.
- Use role-based access to secure data warehouses.

---

## 📞 **Contact**

For any queries or feedback, reach out to:

- **Name**: Charlie Delgado  
- **College ID**: 20211092  
- **Email**: charliedelgado12@icloud.com


