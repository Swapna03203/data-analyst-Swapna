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

**Project Title:** Data Wrangling for Accident Reporting Records Using AWS Services

**Objective:** The aim of data wrangling is to clean the sample data extracted from the Accident Reporting Records dataset. This involves cleansing of data, transforming of data and then aggregating the data in other to enhance the quality and suitability for further data analysis processing. The whole process of wrangling will be automated, safeguarded, and overseen by AWS tools.

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
**loudWatch:**
Set up CloudWatch to keep track on Glue task execution status and S3 bucket activities.
CloudTrail:

Use CloudTrail to keep track of all AWS API activity for security and auditing.


      
      
