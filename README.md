![Logo](https://www.novadrivemotors.com.br/logo.png)


### BRAZILIAN CAR DEALERSHIP

#### **Project Overview: Nova Drive Brazilian Car Dealership**

#### **Introduction**

Nova Drive is a burgeoning car dealership in Brazil, selling over 200 high-value vehicles daily. This impressive sales volume, especially for a new company, underscores the need for robust data management and analytics to sustain growth and enhance operational efficiency.

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
