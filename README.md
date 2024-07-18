![Logo](https://www.novadrivemotors.com.br/logo.png)


# BRAZILIAN CAR DEALERSHIP PROJECT

#### **Project Overview: Nova Drive Brazilian Car Dealership**

#### **Introduction**

Nova Drive is a burgeoning car dealership in Brazil, selling over 200 high-value vehicles daily. This impressive sales volume, especially for a new company, underscores the need for robust data management and analytics to sustain growth and enhance operational efficiency.

## Proposed Architecture

![App Screenshot](https://github.com/Marckelson/BRAZILIAN-CAR-DEALERSHIP/blob/master/DataEngineering_Project.png)

The proposed architecture involves building an application with a PostgreSQL database that updates sales data every minute. The main goal is to transfer data from this operational database to an analytical layer in Snowflake, a data warehouse.

1. **Operational Database (PostgreSQL):** Stores sales data, including information about vehicles, customers, salespeople, and dealerships. It's not ideal for analytical purposes due to its structure aimed at maintaining data integrity and handling frequent updates.

2. **Analytical Database (Snowflake):** Designed for analytical processing, offering high read performance and used for decision-making, reports, machine learning, and dashboards.

3. **Data Pipeline:**

- **Staging Area:** Intermediate storage in Snowflake where data from the operational database is initially loaded.
- **Transformation:** Data in the staging area is transformed using dbt (data build tool) into an analytical format. This transformation is done within Snowflake for performance and accessibility, allowing SQL-based transformations rather than relying on more complex Python scripts.
- **Airflow:** Orchestrates the entire ETL (Extract, Transform, Load) process. It manages the workflow, handling dependencies, retries on failures, and notifications.

4. **Infrastructure:**

- **Airflow Installation:** Airflow is installed on a Linux virtual machine (EC2) in AWS, managed via Docker containers. This setup ensures that the Airflow instance runs reliably in the cloud without requiring a managed service.
- **DBT:** Utilized within Snowflake to transform data from the staging area to the analytical layer.

This architecture ensures minimal impact on the operational database while leveraging Snowflake's performance for analytical tasks.

#### **Objective**

The primary objective of this project is to implement a comprehensive data pipeline that transforms raw sales data into actionable insights. This will enable the sales management team to make informed decisions, streamline operations, and ultimately boost sales performance.

#### **Key Components**

1. **Operational Database (PostgreSQL)**

- **Function:** Store real-time sales data, including vehicle details, customer information, and sales transactions.
- **Features:** Updated frequently to reflect new sales, ensuring data is always current.

2. **Data Staging and Transformation**

- **Tools:** Apache Airflow for ETL (Extract, Load, Transform) processes.
- **Process:** Extract data from PostgreSQL, stage it in Snowflake, and transform it for analytical purposes using DBT (Data Build Tool).

3. **Analytical Database (Snowflake)**

- **Function:** Store transformed data in a format optimized for analysis.
- **Features:** Provides high-performance data retrieval, supporting various analytical queries and reports.

4. **Cloud Infrastructure**

- **Platform:** AWS EC2 for hosting the data pipeline.
- **Configuration:** Use Docker to manage and deploy Apache Airflow on a Linux virtual machine.

#### **Tasks and Deliverables**

1. **Data Extraction and Loading**

- Set up PostgreSQL as the source database.
- Implement ETL pipelines using Apache Airflow to load data into Snowflake.

2. **Data Transformation**

- Use DBT to transform raw data into meaningful insights, ensuring data is accessible and useful for business users.

3. **Data Analytics and Reporting**

- Develop analytical reports and dashboards that provide insights into sales by dealership, vehicle, and salesperson, as well as temporal sales trends.
- Ensure data accuracy and consistency to build trust in the reporting system.

4. **User Access and Training**

- Provide access to the analytical database and reporting tools to the sales management team.
- Conduct training sessions to help users navigate and utilize the new system effectively.

#### **Expected Outcomes**

- **Improved Data Accuracy:** Reliable and consistent data that supports accurate reporting and decision-making.
- **Enhanced Sales Insights:** Detailed analysis of sales performance by dealership, vehicle, and salesperson.
- **Temporal Analysis:** Ability to track and analyze sales trends over time, aiding in strategic planning.
- **Operational Efficiency:** Streamlined data management processes reduce manual intervention and errors.

#### **Conclusion**

The implementation of this data pipeline and analytics solution will empower Nova Drive's sales management team with the insights they need to drive performance and growth. By leveraging advanced data tools and cloud infrastructure, the project aims to transform raw sales data into a strategic asset for the company.
