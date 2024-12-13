**Descriptive Analysis of City of Vancouver District Lots**

Project Description	

Project Title

Objective

Dataset	

Methodology	

Tools and Technologies	

Deliverables

**Data Wrangling for City of Vancouver District Lots**

Project Description

Project Title

Objective

Background

Dataset

Methodology 

Tools and Technologies

Deliverables

Timeline

**Data Quality Control of City of Vancouver districts lots**

Project Description

Project Title

Objective

Background

Scope

Methodology

Deliverables

Timeline

**Descriptive Analysis of Occupational Health and Safety Policy at UCW**

Project Description	

Project Title

Objective

Dataset	

Methodology	

Tools and Technologies	

Deliverables

**Data Wrangling for Occupational Health and Safety Policy at UCW**

Project Description

Project Title

Objective

Background

Dataset

Methodology 

Tools and Technologies

Deliverables

Timeline

**Data Quality Control of Occupational Health and Safety Policy at UCW**

Project Description

Project Title

Objective

Background

Scope

Methodology

Deliverables

Timeline




**Descriptive Analysis for City of Vancouver District Lots**

**Project description:**  
This study examines the **district lot counts** and geographic trends in the **City of Vancouver** to provide valuable insights into urban planning and resource allocation. Using AWS services such as **Amazon S3**, **AWS Glue DataBrew**, and **Amazon Athena**, the project enables efficient data intake, cleaning, and analysis. It detects high-density locations, land use distributions (e.g., residential, commercial), and clustering patterns across geographical zones. The findings offer actionable insights for improving zoning, infrastructure development, and resource management. Visualizations such as bar charts and heatmaps provide a clear knowledge of district lot allocations, allowing city planners to make more educated decisions.

**Project Title:** An Analysis of Vancouver's District Lot Distribution


**Objective :**
This research aims to analyze the geographic distribution of district lot counts in the City of Vancouver. This analysis seeks to:
Summarize district lot counts for different geographic locations.
Find patterns or clusters in district lot distribution.
Using AWS cloud services, provide meaningful insights into city planning and resource allocation.

**Dataset**
The dataset offers district lot information for the City of Vancouver, with significant properties such as:

**Geo_Local_Area:** Geographic area name (for example, Downtown, West End, etc.).

**District_Lot_Count:** The number of district lots per geographical region.

**Label:** Classification of land use (for example, residential, business, or industrial).

**Geoms** Coordinates are geographic positions that serve as geographical references.

**Methodology:**

**Data collection and preparation**

**Data Extraction:** Data obtained from Vancouver's Open Data platform.
**Data Ingestion:** The dataset is stored in an Amazon S3 bucket (pad-dis-raw-swa).

**Data cleaning and profiling**
AWS Glue DataBrew is used to clean the dataset,Address any missing values or outliers,Validate data types (for example, numerical counts for district lots).
AWS Glue DataBrew is also used for data profiling the data to ensure its quality.
The cleaned dataset is stored in a transformation bucket (pad-dis-trf-swa).

**Descriptive statistics:**
AWS Glue DataBrew and Amazon Athena were used to generate the following statistics:

**Total District Lots:** Determine the total number of district lots in all geographic locations.

**Top Geographic places:** Determine which places have the biggest amount of district lots.

**Distribution by Land Use:** Determine the proportion of residential, commercial, and industrial parcels.

**Periodic Variations:** Check for seasonal or monthly changes in district lot numbers (if available).


**Data Exploration and Analysis:**

**Amazon Athena.**
Queries were used to investigate district lot numbers and their correlation with land use categories.Patterns from several locations were retrieved using SQL-based searches.

**Clustering and Spatial Analysis:** We evaluated geographic data to detect trends in district lot counts, such as larger numbers in downtown regions.Key information were visually shown to support city planning decisions 

**Insight and Findings**
Downtown and the West End have the largest concentrations of district lots.  

Residential land use dominated most locations, with commercial properties concentrated in core zones.  

District lot clusters were located in central city locations and decreased as you moved into outlying communities.

Minor fluctuations in district lot activity were seen during the spring and summer months, owing to probable building projects.  

**Recommendations**

Examine land use in high-density regions to guarantee a mix of residential, business, and recreational uses.  

Prioritize regions with high district lot counts for better infrastructure development.  

Prioritize maintenance and planning resources for key locations with dense lot populations.  

Use other data, such as population density or development permits, to gain deeper insights.  

**Insights and findings**
Downtown and West End have the largest concentrations of district lots.  

The majority of the property was used for residential purposes, with commercial lots concentrated in key regions.  

District lot clusters were abundant in central city locations, but decreased as you moved to outlying communities.  

Minor fluctuations in district lot activity were detected during the spring and summer months as a result of anticipated building projects.  

**Recommendations**

Evaluate land use in high-density locations to provide a mix of residential, commercial, and recreational spaces.  

Concentrate on locations with high district lot counts for better infrastructure development.  

Prioritize maintenance and planning efforts in key locations with high lot densities.  

To gain deeper insights, integrate other data such as population density or development permits.  

**Tools and Technologies:**

**Amazon S3:** Used to store raw and converted data.

**AWS Glue DataBrew:** Used for data cleansing, profiling, and transformation.

**Amazon Athena:** Used to query and derive insights from a dataset.


**Deliverables:**

-Deliverables include a complete report outlining the study process, findings, and suggestions.  

-District lot numbers, geographic clusters, and land use patterns are represented using visualizations such as pie charts, bar charts, and heatmaps.  

- Datasets were cleaned and organized before being saved in Amazon S3 for future analysis and decision making.  

- An overview of critical insights, trends, and concrete initiatives for city planners and stakeholders.  

- AWS logs and data pipelines for auditing and validation.  

- Data documentation describing the sources, cleaning stages, and transformation processes.

![image](https://github.com/user-attachments/assets/b9914f34-4378-4d97-86b7-3035b2a19882)


**Data Wrangling for City of Vancouver District Lots**

  **Project Description**
The goal of this project is to guarantee correctness, consistency, and usefulness for spatial research and urban planning by **data wrangling** the City of Vancouver's district lot information. The project uses **AWS tools** such as Amazon S3, Glue DataBrew, and Athena to clean, convert, and consolidate data, resulting in a strong dataset for studying district lot distributions, geographic trends, and land use classifications. Missing value management, format standardization, and the development of additional features such as lot density are all important challenges. The final deliverables include a cleaned dataset, infographics, and interactive dashboards to aid in informed decision-making for zoning optimization and resource allocation.

**Project Title:** Data Wrangling for Optimal District Lot Insights and Urban Planning.

**Objective**
The goal of this project is to do end-to-end data wrangling on the City of Vancouver's district lot data to assure correctness, completeness, and usability. The cleaned and consolidated information will allow for effective spatial analysis, revealing land use trends, identifying regional patterns, and assisting with urban planning choices such as zoning and resource allocation.

**Background**
The City of Vancouver gathers and administers district lot data from a variety of geographic locations, including district lot numbers, land use classifications (residential, commercial, and industrial), and geographical coordinates. However, the dataset's discrepancies, missing numbers, and formatting flaws restrict its usefulness for urban development programs.

**Dataset**
The project is focused on the following important attributes:

**Geo_Local_Area:** Geographic area names (for example, Downtown, West End, or Kitsilano).

**District_Lot_Count:** The total number of district lots in each geographical area.

**Label:** A classification of land use (for example, residential, commercial, or industrial).

**Geoms:** Latitude and longitude values corresponding to district lot locations.

**Methodology**

**Data Collection**
The district lot data is available through the City of Vancouver's Open Data portal.
Upload the raw dataset to the Amazon S3 bucket (district-lots-raw-swa) for centralized and safe storage.
With AWS KMS encryption and S3 bucket versioning, you can provide version control and data security.

**Data Assessment**
Use AWS Glue DataBrew to examine the dataset's quality.
      Find missing data in properties like district lot counts or locations.
      Detect and document duplicate records.
      Examine data formats for irregularities (for example, incorrect date formats or misspelled Geo_Local_Area names).
      Create data profiles that summarize significant information (e.g., minimum, maximum, and average lot counts).

Log and document any discoveries, including inconsistencies, oddities, and places that need cleaning.

**Data Cleaning**

**Address the missing values:**
Use averages or regional medians to fill in missing District_Lot_Count data, where appropriate.
Remove or mark records with missing coordinates for spatial analysis.
Remove duplicate records using unique Geo_Local_Area and Coordinate combinations.

**Standardize the data formats:**
Correct date and timestamp formats to ensure uniformity.
Normalize categorical variables.
Standardize the land_use_label (e.g., residential, commercial, industrial).
Correct discrepancies in Geo_Local_Area names (for example, "Downtown" vs. "downtown").
Clean data should be stored in a transformation bucket (pad-dis-trf-swa) on Amazon S3 for further processing.

**Data Transformation and Cleaning (AWS Glue DataBrew):** Transform and clean the district lot dataset using **AWS Glue DataBrew**.  

- **Address Missing Values**: Impute or replace missing values in critical variables like **District_Lot_Count** (e.g., use median or average) and **Land_Use_Label** (replace with "Unknown").  
- **delete Duplicates**: Identify and delete duplicate items based on **Geo_Local_Area** and **Coordinates** to maintain data integrity.  
- **Format Correction**: - Convert **Timestamp** to proper 'datetime' format for precise temporal analysis.  
   - To ensure consistency, capitalize each term in **Geo_Local_Area** and **Land_Use_Label**. For example, "downtown" → "Downtown"  
- **Feature Engineering**: - Create new columns, such as **Lot Density** (calculated as District_Lot_Count per unit area if area size data is provided).  
   
This structured data transformation produces a clean, enhanced, and consistent dataset, allowing for reliable downstream analysis and reporting.  


**Data Consolidation With Amazon Glue (Visual ETL) and DynamoDB:**  
Import the cleaned and enhanced district lot dataset into a **Visual ETL pipeline** using **AWS Glue**. The schema has five key attributes: **Geo_Local_Area** (the primary key), **District_Lot_Count**, **Land_Use_Label**, **Coordinates**, and **Timestamp**.  
The processed data is stored in **DynamoDB**, which allows for quick searching and retrieval for geographical analysis, land-use clustering, and future research.


**Monitoring and Security:** **IAM and KMS:** - Enforce access policies for S3 buckets, Glue jobs, and DynamoDB tables using AWS Identity and Access Management (IAM).  
- **AWS Key Management Service (KMS)** guarantees that all data at rest, including S3 and DynamoDB, is secured.

**Cloud Watch**
Configure Amazon CloudWatch to monitor Glue ETL job execution status, S3 bucket performance (including activity logs and storage utilization), and DynamoDB read/write capacity.  

**CloudTrail:**
Implement AWS CloudTrail to log all AWS API activities for auditing, change tracking, and security compliance across Glue, S3, and DynamoDB.
This connection offers safe, efficient, and monitored data processing while ensuring compliance and allowing for scalability during analysis.



**Tools and technologies.**

**Amazon S3:** provides storage for both the raw and sanitized datasets.

**AWS Glue:** Data catalog development and transformation tasks.

**AWS Glue DataBrew:** AWS Glue DataBrew cleans and transforms data.

**Athena:** Amazon Athena enables data querying and validation.

**Amazon DynamoDB:** Amazon DynamoDB provides storage for accident records that have been cleansed and converted.

**Cloud Watch** CloudWatch monitors Glue job activity and system performance.

**Cloud Trail** CloudTrail logs AWS activity for security and auditing purposes.

**IAM and KMS** IAM and KMS provide secure data access and encryption.


**Data Quality Control for City of Vancouver District Lots**

**Project Description:** This project aims to create a Data Quality Control (DQC) framework for the City of Vancouver District Lot Dataset utilizing AWS services. This program assures that the dataset is correct, comprehensive, consistent, and dependable for urban planning, zoning optimization, and infrastructure choices. This project uses AWS resources such as S3, Glue, DataBrew, Athena, DynamoDB, CloudWatch, and CloudTrail to execute rigorous data profiling, cleansing, validation, monitoring, and reporting procedures that ensure data integrity and allow informed decision-making.

**Project Title:** Implementing Quality Control Measures for District Lot Data with AWS.

**Background:** The City of Vancouver's district lot information is important for urban planning, however it has missing values, duplicate entries, and inconsistent formats, making it less usable. These difficulties can result in inaccurate zoning analysis, resource misallocation, and insufficient insights. To address these issues, this project provides a complete Data Quality Control framework that uses AWS capabilities to assure data quality, real-time integrity monitoring, and the creation of a long-term structure for data governance.

**Scope:** The Data Quality Control Initiative addresses:

**Data Profiling:** Data profiling is the process of determining whether or not data is comprehensive, correct, and consistent.

**Data Cleaning:** Data cleansing include removing duplicates, rectifying mistakes, and standardizing formats.

**Data Profiling:** Data validation is the process of putting standards in place to guarantee that data remains accurate over time.

**Data Monitoring** Monitoring and reporting involve creating dashboards and alerts for real-time tracking

**Data Protection:** Data Protection entails ensuring encryption and safe access to data resources.

**Training:** Training involves educating stakeholders about data quality management and best practices.

**Methodology**

**Phase I: Data Ingestion and Storage (Week 1)**
Upload the district lot dataset to Amazon S3 (district-lots-raw-swa) to ensure centralized storage.
Configure IAM roles to ensure safe access to S3 buckets.
Allow S3 versioning to save previous versions of the dataset for rollback and auditing.

**Phase II: Data Profiling (Week 2)**
Use AWS Glue Crawler to profile the dataset and catalog information in AWS Glue.
Use AWS Glue DataBrew to evaluate data completeness, uniqueness, consistency, and correctness.
Find missing values in District_Lot_Count and Land_Use_Label.
Detect duplicate data using Geo_Local_Area and coordinates.

**Phase Three: Data Cleaning (Week 3–4)**
AWS Glue DataBrew will be utilized to clean and modify the dataset:Remove duplicate data based on Geo_Local_Area and coordinates,Imput missing values,Replace a missing Label with "Unknown." To fill in lacking District_Lot_Count, use the average/median value.
Standardise and format:Convert the timestamp to the suitable datetime format.
Normalize Label (e.g., capitalize values like "residential" to "residential").
Finally ,Place the cleaned dataset in Amazon S3 (pad-dis-trf-swa).

**Phase 4: Data Validation (Week 5)**
Set up validation rules in AWS Glue to ensure:
Geo_Local_Area entries have no duplicates.
Consistency: District_Lot_Count has only correct numeric values.
Categorical Compliance: Compare Land_Use_Label to an approved list (e.g., residential, commercial, industrial).
Use Amazon Athena to query S3 buckets and ensure the clean dataset's integrity.

**Phase Five: Data Enriching and Protection (Week 6).**

**Data Enriching:**
Import the cleaned and verified dataset into Amazon DynamoDB to perform organized and efficient queries.
Schema includes:The primary key is Geo_Local_Area, and the attributes are District_Lot_Count, Land_Use_Label, Coordinates, Timestamp, and Validation Status.

**Data Protection:** The **City of Vancouver's district lot dataset** is safe and compliant thanks to strong data security. Data integrity is protected through the use of **AWS KMS** encryption, **IAM** access control, and **S3 versioning** backups. **CloudTrail** and **CloudWatch** offer monitoring and logging capabilities, assuring confidentiality, security, and compliance with governance requirements.


**Phase Six: Monitoring and Reporting (Week Seven)**
Enable Amazon CloudWatch to monitor:Integrate job execution statuses with data transformation pipeline performance.
Use AWS CloudTrail to record all API interactions for auditing and security purposes.
Create real-time dashboards using CloudWatch or Athena queries to visualize:
Duplicate records, missing values, and format compatibility.
Data quality trends include critical parameters (such as error rates and completeness).

**Phase Seven: Training and Awareness (Week Eight)**
Create training materials and seminars for city planning and data teams to teach them about data quality concepts.
Showcase AWS technologies for ensuring data integrity.
Establish criteria for uniform data entry and quality management.
Create a culture of accountability for continual data quality improvement.

**Tools and Technologies:**

**Amazon S3:** Amazon S3 provides secure storage for raw, converted, and verified datasets.

**AWS Glue and Glue DataBrew:** AWS Glue and Glue DataBrew provide data profiling, cleansing, transformation, and validation.

**Amazon Athena:** Amazon Athena supports SQL queries for integrity checks and analysis.

**Amazon DynamoDB:** Amazon DynamoDB provides storage for condensed and organized datasets.

**Amazon CloudWatch:** Amazon CloudWatch provides real-time monitoring of Glue tasks and S3 operations.

**AWS CloudTrail**AWS CloudTrail audits all API operations for compliance.

**IAM and KMS:** IAM and KMS provide secure access and data encryption 

**Deliverables**

**Cleaned Dataset:** Cleaned and validated The dataset is stored in Amazon S3 (CSV and Parquet) and DynamoDB for structured access.
**Data Quality Metrics Report:** Detailed documentation for completeness, correctness, duplication, and mistakes.
**Monitoring Dashboard:** Real-time display of data quality measures (for example, missing values and error patterns).
**Process Documentation:** A detailed study on data quality methodologies, tools, and KPIs.
**Training Materials and Workshops:** Resources for educating teams about data quality best practices and AWS technologies.


**Timeline**
**Week 1:** Data intake and storage configuration on Amazon S3.

**Week 2:** Data profiling using AWS Glue Crawler and Glue DataBrew.

**Weeks 3–4:** Data cleaning and transformation using Glue DataBrew.

**Week 5:** Data validation and integrity checks using Glue and Athena.

**Week 6:** Data enrichment and protection using DynamoDB for structured querying and IAM & KMS for data security.

**Week 7:** Configuring CloudWatch and CloudTrail for monitoring and creating dashboards.

**Week 8:** Workshops for stakeholders on data quality procedures.

This Data Quality Control program for the City of Vancouver's district lot dataset guarantees that data used in urban planning and decision-making is clean, verified, and trustworthy. By utilizing AWS services for profiling, cleaning, monitoring, and training, the project improves data quality, simplifies compliance, and provides municipal planners with relevant information.


![image](https://github.com/user-attachments/assets/f4299b57-e04d-4919-bbac-fe266e8b7c73)











**Descriptive Analysis of Occupational Health and Safety Policy at UCW**

**Project Description:** Descriptive Analysis of Occupational Health and Safety Policy for Compliance and Optimization

**Project Title:** Understanding Health and Safety Policies in University Canada West

**Objective:** The primary goal is to conduct a descriptive analysis of the UCW Occupational Health and Safety Policy to extract structured insights, ensure regulatory compliance, and enable efficient management using AWS cloud services.
This project will:
-Summarize key sections and responsibilities in the policy.
-Structure the data for accessibility and management in AWS.
-Provide visualized insights to enhance understanding and support compliance.

**Dataset:** The dataset will be derived from chatgpt, including the following information:

**Incident_Date:** Time of occurrence of the particular event.

**Incident_Type**: Categorisation of the event (for instance Near Miss, Injury or Illness).

**Worker ID:** General identifier of the worker which was effected by the occurrence.

**Report_ID:** General identifier of the report

**Report_Submission_Date:** Time report was submitted 


**Methodology:**

**Data Collection and Preparation:**

**Data Extraction:** Relevant data has to be obtained from Chatgpt.

**Data Ingestion:** The excel downloaded should then be uploaded into the Amazon S3 bucket hr-acc-raw-swa.t (hr-acc-raw-swa).

**Data Cleaning and Data Profiling:** For data cleaning and data profiling I made project in AWS Glue Databrew . This could be via automatic connectors provided with the kit, or writing scripts by hand.With regards to Data cleaning, perform descriptive statistics and eliminate the missing values, and outliers in the Profiling step.Deliver the extracted information in a useable for analysis form, and save the information to the different bucket (hr-acc-trf-swa).

**Descrptive Statistics:**
Using AWS Glue DataBrew we can identify 
-Total of all the incidents that are recorded in the observation chart.
-Discover what types of cases are most often reported.
-Document periodic variations in the rate of occurrence of incidents.


![image](https://github.com/user-attachments/assets/90fb05c2-4f7b-425b-9c88-b0f710fcb8f3)


**Data Exploration and Analysis:** In the next process, Amazon Athena was utilized as a tool to extract data by querying from DynamoDB.

**Insights and Findings:**
All the accident reports were filed within one day, which shows that reporting in their organization is effective.
The dataset includes three types of accidents:
      Slip and Fall
      Equipment Malfunction
      Exposure to Chemicals
This variety indicates the need for safety practices in various segments of operations.
Some of the accidents took place in January, March and May although due to small sample size it is difficult to infer seasonal differences.

**Recommendations:**
**Safety Training:** Provide specific training sessions to correspond to all frequent types of accidents that occur on the workplace, for instance, falling, equipment utilization, and chemical use.
**Incident Analysis:** That way, efforts to understand the causes of these accidents in order to prevent them will be worthwhile.
**Expand Data Collection:** Delay the use of the system for sometime and collect more data to be used in analyzing for trends and period which most patients are vulnerable.

**Tools and Techniques:**
**Amazon S3**: For storing the data extracted.

**AWS Glue DataBrew:** To pre-processed data from the excel sheet and convert it into standard format like CSV and then store the data in some data storage service.

**Amazon Athena:** To filter the returned results of DynamoDB and to get the related stats.

**Deliverables:**
-The detailed report that contains the description of the analysis methods, results, and conclusions.
-Dashboards and visualizations are enabled through interaction using AWS tools. 
-A presentation is made to disseminate the outcome and suggestion of the research to the stakeholders.

      This descriptive analysis leverages AWS services to efficiently analyze the occupational health and safety data, providing valuable insights to improve workplace safety at UCW.

**Data Wrangling of Occupational Health and Safety Policy at UCW**

**Project Description:** Data Wrangling for Accident Reporting Records at University Canada  West .This project seeks to convert the raw dataset into a clean, consolidated format that will allow for speedy retrieval, accurate analysis, and compliance reporting by organizational stakeholders. The data wrangling process will be automated and monitored using AWS services such as S3, Glue, DataBrew, DynamoDB, Athena, CloudWatch, and CloudTrail, all while ensuring data security and control.

**Project Title:** Data Wrangling for Accident Reporting Records Using AWS Services

**Objective:** The aim of data wrangling is to clean the sample data extracted from the Accident Reporting Records dataset. This involves cleansing of data, transforming of data and then aggregating the data in other to enhance the quality and suitability for further data analysis processing. The whole process of wrangling will be automated, safeguarded, and overseen by AWS tools.

**Background:** Organizations struggle to manage accident reporting records because the data is fragmented, inconsistent, or incomplete. Accurate reporting and analysis of workplace occurrences is critical for regulatory compliance, hazard identification, and preventative action.The Accident Reporting Records dataset, which contains information such as accident dates, worker IDs, accident kinds, and report submission dates, requires data wrangling. This process comprises data intake, cleansing, profiling, and protection to provide high-quality, dependable data. The wrangling process will be scalable, safe, and efficient thanks to the use of Amazon Web Services.

**Dataset Overview:**
Accident Reporting Records Dataset includes:

**Report_ID:** A number allocated to one particular report only.

**Accident_Date**: Date of the accident.

**Worker_ID:** A ‘‘worker identifier’’ or, if one does not exist, the worker’s name.

**Accident_Type:** Old age (Cohort) – name of type of accident (e.g. Slip and Fall).

**Report_Submission_Date:** Time of submission of the report.

**Methodology:**

**1. Data Collection and Storage (Amazon S3):**
-The Accident Reporting Records will be uploaded in Excel or CSV format to an S3 bucket(hr-raw-swa).
-The important approach is protection of data that can be achieved by controlling access using S3 bucket policies and IAM roles.

**2. Data Assessment (AWS Glue + Athena):**

**AWS Glue Crawler:**
Initialize an ETL job in Glue to crawl the S3 bucket and, upon doing so, create a table schema in the Glue Data Catalog.

**Amazon Athena:**
Use Athena to query the dirty dataset directly from S3 to check for:
Missing values.
Duplicates.
Incorrect date formats.
Register primary problems with data quality after documents’ creation.

**3. Data Transformation and Cleaning (AWS Glue DataBrew):** AWS Glue DataBrew for data transformation and cleaning:
**Address Missing values:** impute or replace the substitute missing Accident_Date or Accident_Type (for example, "Unknown").
**Remove duplicates:** Identify and eliminate any duplicate Report_ID entries.
**Format correction:** Convert Accident_Date and Report_Submission_Date to the correct datetime forms.
Standardize text fields, such as Accident_Type (capitalize each word).
**Feature Engineering:** Generate additional columns like "Submission Delay" (the difference between Accident_Date and Report_Submission_Date).

**4. Data Consolidation using Amazon Glue (Visual ETL) and DynamoDB:**
Import the cleaned dataset into a Visual ETLdatabase using the following schema
The primary key is Report_ID, with attributes including Accident_Date, Worker_ID, Accident_Type, Report_Submission_Date, and Submission_Delay.
DynamoDB facilitates the rapid querying and retrieval of accident information for future study.

**5. Monitoring and Security:**

**IAM and KMS.**
To enforce S3 bucket, Glue job, and DynamoDB access policies, use AWS Identity and Access Management (IAM).
Use the AWS Key Management Service (KMS) to encrypt data at rest.
**CloudWatch:**
Set up CloudWatch to keep track on Glue task execution status and S3 bucket activities.
**CloudTrail:** Use CloudTrail to keep track of all AWS API activity for security and auditing.

**Tools and Technology:**
**Amazon S3:** provides storage for both the raw and sanitized datasets.

**AWS Glue:** Data catalog development and transformation tasks.

**AWS Glue DataBrew:** AWS Glue DataBrew cleans and transforms data.

**Athena:** Amazon Athena enables data querying and validation.

**Amazon DynamoDB:** Amazon DynamoDB provides storage for accident records that have been cleansed and converted.

**Cloud Watch** CloudWatch monitors Glue job activity and system performance.

**Cloud Trail** CloudTrail logs AWS activity for security and auditing purposes.

**IAM and KMS** IAM and KMS provide secure data access and encryption.

**Deliverables**
Cleaned and transformed datasets stored in DynamoDB and S3.
Data Quality Report that includes missing values, duplicates, and modifications.
Athena Queries for validating the cleaned data.
Logs & Monitoring Set up CloudWatch and CloudTrail for security and performance monitoring.

**Timeline:**

**Total Duration : 7 Weeks**
The data wrangling process includes six phases: 1) Data Ingestion, 2) Data Analysis, 3) Data Cleaning, 4) Data Profiling, 5) Data Security, 6) Data Consolidation, and 7) Monitoring. The first step is to upload the raw accident reporting dataset to Amazon S3, configure IAM roles and S3 bucket policies for data security, and enable S3 versioning for data version management. The second step comprises data analysis with AWS Glue Crawler and Amazon Athena to find errors such as missing information, duplication, and format inconsistencies. The third phase comprises data cleaning with AWS Glue DataBrew, which addresses missing values, removes duplicate entries, standardizes date formats, and cleans up 'Accident_Type' text fields. The fourth process comprises data profiling, which validates the cleaned data and ensures its correctness, consistency, and completeness.The fifth phase entails data security with AWS KMS and IAM rules for S3 and DynamoDB. The sixth process entails data consolidation, saving the cleansed data in Amazon DynamoDB for future analysis, and retaining unique IDs.

The goal of this data wrangling is to create a **high-quality, clean, and organized dataset** for the **Accident Reporting Records**, which will allow for effective incident analysis and compliance monitoring. The project will enable trustworthy reporting and insights by resolving data quality concerns, standardizing formats, and safeguarding the data with AWS services. This will assist the firm in identifying workplace dangers, improving safety practices, ensuring regulatory compliance, and driving overall improvement in workplace safety management.

![image](https://github.com/user-attachments/assets/d8b8b73e-ff0d-4cec-9994-a5f6308bcbe7)

**Data Quality Control Measures of Occupational Health and Safety Policy at UCW**

**Project Description:** The major goal of this project is to provide a Data Quality Control (DQC) framework for the Accident Reporting Records dataset utilizing AWS services. This framework will guarantee that incident data is accurate, full, consistent, and reliable, allowing the business to discover safety gaps, comply with requirements, and make better workplace safety decisions. This project will use AWS resources such as S3, Glue, DataBrew, DynamoDB, Athena, CloudWatch, and IAM to create a strong process for profiling, cleaning, validating, and monitoring data quality.

**Project Title:** Implementing Data Quality Control Measures for Accident Reporting Records Using AWS

**Background**
Organizations rely on precise and trustworthy accident reporting data to detect workplace dangers, resolve safety events, and maintain regulatory compliance.However, issues like as errors, missing values, duplicate entries, and incompatible formats might jeopardize data integrity. Poor data quality might result in inefficient incident management and delayed remedial measures.To solve these issues, the project will use AWS services to perform rigorous Data Quality Control (DQC) techniques. This program will enhance the accuracy of accident records, monitor data integrity in real time, and develop a culture of accountability for data quality.

**Scope**
The Data Quality Control Initiative will include:

Data profiling involves evaluating data quality in terms of completeness, correctness, and consistency.
Data cleansing include removing duplicates, standardizing formats, and filling in missing information.
Data validation is the process of putting standards in place to guarantee that data remains accurate over time.
Monitoring and reporting: Developing dashboards and alerts for real-time data quality tracking.
Data Protection-Ensuring the secure access and encryption of accident data.
Training-Educating employees on data quality methods and best practices.

**Methodology**

**Phase One: Data Ingestion and Storage (Week 1)**
Upload the Accident Reporting Records data set to Amazon S3.
Configure IAM roles to limit access and increase security.
Enable S3 versioning to preserve historical documents.

**Phase Two: Data Profiling (Week 2)**
Use AWS Glue Crawler to profile the dataset and add it to the Glue Data Catalog.
Use AWS Glue DataBrew to assess data completeness, uniqueness, validity, consistency, and correctness.
Issues with document data quality include missing values, duplicate records, and inconsistent formats.

**Phase 3: Data Cleansing and Transformation (Week 3–4)**
Use AWS Glue DataBrew to remove duplicate records based on Report_ID.
Standardize the date formats for Accident_Date and Report_Submission_Date.
Fill in missing data with suitable placeholders (for example, "Unknown Accident Type").
Normalize categorical variables such as Accident_Type.
Place the cleansed dataset back on Amazon S3.

**Phase 4: Data Validation (Week 5).**
Implement validation rules in AWS Glue to ensure unique Report_ID entries.
Dates should be formatted properly using datetime.
Consistent values for categorical variables such as Accident_Type.
Use Amazon Athena to query and check the integrity of S3 buckets.

**Phase 5: Data Consolidation (Week 6).**
Import the cleaned and verified dataset to Amazon DynamoDB using:
The primary key is Report_ID, and the attributes include accident information, submission delays, and validation status.

**Phase 6: Monitoring and Reporting (Week 7).**
Set up alerts in Amazon CloudWatch to track the status and performance of your Glue jobs.
AWS CloudTrail tracks and logs all dataset-related activity for auditing reasons.
Create data quality dashboards using Amazon QuickSight or Athena queries.
Duplicate records accumulate over time.
Missing values and trends.
Real-time data quality metrics.

**Phase 7:Training and Awareness (Week Eight)**
Create training materials and hold workshops for staff on data quality best practices.
Use AWS tools to ensure data integrity.
Data entry recommendations for minimizing mistakes.


**Tools and Technologies**

Amazon S3 provides secure storage for raw and processed datasets.
AWS Glue and Glue DataBrew provide data profiling, cleaning, and transformation.
Amazon Athena: querying and verifying datasets.
Amazon DynamoDB stores the cleaned and verified dataset.
CloudWatch monitors Glue task performance and data quality parameters.
CloudTrail logs all AWS activity to ensure security and audit compliance.
IAM and KMS provide secure access management and data encryption.

**Deliverables**

Cleaned and validated The dataset is stored in Amazon S3 and DynamoDB.
Data Quality Metrics Report on completeness, duplication, and mistakes.
A monitoring dashboard is used to track data quality indicators in real time.
Documentation of the data quality control procedure, including methodologies and instruments.
Employee training materials and workshops on data quality management.

**Timeline**

**Week 1:** Data intake and storage on Amazon S3.

**Week 2:** Data Profiling with AWS Glue Crawler and DataBrew.

**Weeks 3–4:** Data purification and transformation using AWS Glue DataBrew.

**Week 5:** Data validation and integrity checks with Glue and Athena.

**Week 6:** Data is consolidated into DynamoDB for structured access.

**Week 7:** covers monitoring and reporting with CloudWatch, CloudTrail, and QuickSight.

**Week 8:** Train employees on data quality protocols and best practices.







 



      
      





      
      
