# DATA-226-ASSIGNEMNT-6
# 📊 Weekly Active User (WAU) Analysis

## 📘 Overview
This project implements an end-to-end data pipeline and analytics workflow using **Apache Airflow**, **Snowflake**, and a **Business Intelligence (BI)** tool.  
The objective is to generate and visualize the **Weekly Active User (WAU)** metric from session data through ETL, ELT, and dashboard creation processes.

---

## 🧩 Tasks Performed

### 1. ETL DAG Creation (Airflow)
- Imported two tables into **Snowflake**:
  - `user_session_channel`
  - `session_timestamp`
- Designed an **ETL DAG** in **Apache Airflow** to load the above tables under the `raw` schema (or an equivalent schema).
- Captured a screenshot of the DAG’s detailed page from the **Airflow Web UI**.  
  📷 *Screenshot #1 — ETL DAG*

---

### 2. ELT DAG Creation (Airflow)
- Developed an **ELT DAG** in **Apache Airflow** to join the two imported tables and create a new table named `session_summary` under the `analytics` schema.
- Added an **additional condition** to check for duplicate records in the data pipeline.
- Captured a screenshot of the DAG’s detailed page from the **Airflow Web UI**.  
  📷 *Screenshot #2 — ELT DAG*

---

### 3. Preset Account Setup
- Configured a **Preset** account and established a **Snowflake connection**.
- Imported the `session_summary` table generated from the ELT DAG.
- Captured a screenshot of the dataset view in **Preset**.  
  📷 *Screenshot #3 — Dataset View*

---

### 4. WAU Chart Creation (BI Tool)
- Created a **Weekly Active User (WAU)** chart using the BI tool (Preset/Tableau/Power BI).
- Renamed the metric field to **WAU** for clarity.
- Captured a screenshot of the final WAU visualization.  
  📷 *Screenshot #4 — WAU Chart*

---

## 📂 Repository Structure
```text
├── dags/
│ ├── etl_user_session_dag.py
│ ├── elt_session_summary_dag.py
├── screenshots/
│ ├── airflow_etl_dag.png
│ ├── airflow_elt_dag.png
│ ├── preset_dataset.png
│ ├── wau_chart.png
├── README.md
```

---

## 💡 Notes
- This assignment demonstrates the workflow of **data extraction, transformation, and visualization** using **Airflow**, **Snowflake**, and **Preset**.
- All screenshots are stored in the `screenshots/` folder.
- All DAG scripts (`ETL` and `ELT`) are stored under the `dags/` directory.
- The WAU chart reflects aggregated user activity data over weekly intervals.

---

## 🧠 Learning Outcomes
- Gained practical experience with **ETL/ELT pipelines** in Airflow.
- Understood data integration with **Snowflake**.
- Created **interactive dashboards** using a BI tool.
- Applied data validation techniques to ensure data quality.
