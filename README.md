# yelpdatanalysis
Perform a Data Analysis on Yelp Data set using Azure Data Factory and Azure Databricks

#Business Overview
In today’s data-driven landscape, leveraging community-driven datasets is essential for organizations to enhance consumer experience and derive business insights. One such dataset is the Yelp dataset, which offers extensive information on local businesses, customer reviews, and user interactions. This dataset serves as a valuable resource for research and analytical projects.

Yelp provides services such as Yelp Reservations, enabling users to discover, review, and book services across diverse sectors, including restaurants, retail, healthcare, and entertainment. To foster innovation, Yelp launched the Yelp Dataset Challenge, offering a curated dataset for researchers, analysts, and developers.

This project establishes a robust data pipeline that integrates raw Yelp JSON files into Azure Data Lake Storage Gen2 as a centralized repository. Azure Data Factory’s Copy Data pipeline orchestrates data movement between storage containers, ensuring structured organization for downstream processing. Azure Databricks is leveraged for transformation and analysis, extracting insights from business, review, and user data. This scalable and efficient Azure-based solution enables seamless processing of Yelp’s vast historical data.

#Project Aim
The primary goal of this project is to process and analyze Yelp’s raw JSON dataset to extract actionable insights related to businesses, customer reviews, and user behavior using Azure services. The dataset is transformed and standardized through a scalable Azure data pipeline to ensure efficient data processing.

##Key Objectives:

	• Ingest raw Yelp data into Azure Data Lake Storage Gen2.
	• Utilize Azure Data Factory’s Copy Data pipeline for seamless data movement.
	• Perform extensive data transformation and analysis using Azure Databricks.
	• Extract insights such as top-performing business categories, customer sentiment trends, and regional business patterns.

##Tech Stack

	• Programming: SQL, Python
 
	• Library: PySpark
 
	• Cloud Services:
 
		○ Azure Data Lake Storage Gen2 (ADLS Gen2)
  
		○ Azure Data Factory (ADF)
  
		○ Azure Databricks
  

#Azure Services Overview
##Azure Data Lake Storage (ADLS Gen2)
Azure Data Lake is a cloud-based platform that supports big data analytics, offering unlimited storage for structured, semi-structured, and unstructured data. Built on Azure Blob Storage, it provides low-cost, tiered storage, high availability, and disaster recovery capabilities. ADLS seamlessly integrates with other Azure services, making it ideal for data processing and analytics.
##Azure Data Factory (ADF)
Azure Data Factory is a cloud-based data integration service that enables ETL (Extract-Transform-Load) and ELT (Extract-Load-Transform) pipelines. It facilitates data movement between various sources, whether on-premises or cloud-based, and ensures seamless data transformation and storage for further analysis.
##Azure Databricks
Azure Databricks is an Apache Spark-based data analytics platform optimized for Azure. It enhances innovation by integrating data science, engineering, and business analytics within a collaborative environment. Databricks accelerates data transformation, machine learning workflows, and large-scale data processing, making it a powerful tool for this project.

#Dataset Overview
This project utilizes the Yelp dataset, which includes key business, review, and user data, facilitating in-depth analysis of customer behavior, business performance, and market trends. The dataset, available in JSON format, consists of the following files:
	1. business.json – Contains details about businesses, including name, location, category, and operational status.
	2. review.json – Includes customer reviews with ratings and timestamps, providing insights into customer sentiments.
	3. user.json – Stores user activity data, including the number of reviews posted and social connections.
	4. checkin.json – Tracks customer check-in data, revealing foot traffic patterns and peak hours.
	5. tip.json – Captures short user suggestions and feedback about businesses.
Together, these files provide a holistic view of the Yelp ecosystem, enabling data-driven decision-making.

#Project Approach
##1. Data Storage Setup
	• Created two Azure Data Lake Storage (ADLS Gen2) containers within the same storage account for structured data storage and processing.
	• Downloaded the raw Yelp dataset (JSON format) and uploaded it to the first ADLS container as the raw data repository.
##2. Data Ingestion & Movement
	• Provisioned Azure Data Factory (ADF) and set up a Copy Data pipeline to move data from the first ADLS container to the second ADLS container, preparing it for analysis.
##3. Data Processing & Transformation
	• Deployed an Azure Databricks workspace and cluster to process and analyze the dataset.
	• Pulled data from the second ADLS container into Databricks for extensive data transformation, cleaning, and analysis.
	• Performed schema validation, partitioning, and coalescing to optimize data storage and query performance.
##4. Data Analysis & Insights
	• Conducted comprehensive data analysis to uncover insights:
		○ Top 3 most active users based on review counts.
		○ Top 10 business categories ranked by number of reviews.
		○ Top businesses with over 1,000 reviews, highlighting customer engagement levels.

#Key Takeaways
	• Understanding real-world data use cases and the Yelp dataset structure.
	• Gaining hands-on experience with Azure services for data storage, movement, and analytics.
	• Building an end-to-end Azure Data Pipeline for data ingestion, transformation, and processing.
	• Learning best practices for data partitioning, coalescing, and transformation in PySpark.
	• Extracting meaningful insights to drive business intelligence and consumer trend analysis.

#Best Practices & Cost Management
	• Monitor Azure services usage to optimize costs and prevent unnecessary expenditures.
	• Leverage auto-scaling in Azure Databricks to dynamically adjust compute resources based on workload.
	• Utilize Azure cost management tools to track and manage expenses efficiently.

#Architecture Diagram
A visual representation of the Azure-based Yelp dataset analysis pipeline, illustrating data flow from ingestion to transformation and insight extraction.
![image](https://github.com/user-attachments/assets/fa0a7885-9f62-437a-9e38-9cd8ec0df5cf)
