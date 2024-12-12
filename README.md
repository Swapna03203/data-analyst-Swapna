**Descriptive Analysis of Occupational Health and Safety Policy at UCW**
Project Description	
Project Title
Objective
Dataset	
Methodology	
Tools and Technologies	
Deliverables

**Descriptive Analysis**

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

**Data Wrangling**
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

**Data Quality Control Measures:**

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





 



      
      





      
      
