# Centralized Healthcare Data Platform 🏥

> **Disclaimer:** *This repository is a portfolio case study. The actual codebase, proprietary data, and specific business logic remain confidential in compliance with Non-Disclosure Agreements (NDAs). The architectural patterns and methodologies described below represent my personal contributions to the enterprise solution.*

## 📖 Project Overview
This enterprise project focused on building a centralized, metadata-driven ingestion platform for the healthcare sector. The goal was to unify highly sensitive data from various healthcare management systems (HCHB, Athena, UKG, Rest API) into a single source of truth for compliance and analytics.

## 🛠️ Technology Stack
* **Orchestration & ETL:** Azure Data Factory (ADF), Azure Logic Apps
* **Storage & Data Warehouse:** Snowflake, SQL Server
* **Security & Governance:** Azure Key Vault
* **Data Sources:** REST APIs, SFTP, RDBMS

## 🏗️ Architecture & Methodology
### Metadata-Driven Framework
* **Master-Child Architecture:** Architected a dynamic, metadata-driven ETL framework within Azure Data Factory. Instead of hardcoding pipelines, the master pipeline dynamically triggers child pipelines based on control table configurations.
* **Dynamic Extraction:** Engineered flexible extraction logic utilizing ADF Switch activities to seamlessly route and process data from diverse sources including SQL Server databases, external REST APIs, and secure SFTP servers.
* **Security First:** Integrated Azure Key Vault natively into the pipelines to handle all credential management and API authentication securely.

### Monitoring & Operations
* Designed a centralized auditing mechanism tracking pipeline runs, row counts, and performance metrics directly within Snowflake.
* Implemented automated, real-time alerting systems using **Azure Logic Apps** to immediately notify operations teams of any pipeline anomalies.

## 🚀 Key Achievements & Impact
* **Reduced Onboarding Time by 80%:** The Master-Child metadata architecture allowed new healthcare data tables to be added to the pipeline purely via configuration, drastically cutting development time.
* **Minimized Failure Resolution Time:** The integration of Logic Apps and centralized Snowflake auditing provided real-time visibility, allowing the team to catch and resolve data issues before they impacted downstream reporting.

---
*Created by [Nakul Daf](https://www.linkedin.com/in/nakul-daf/) | Data Engineer*
