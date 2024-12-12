**Project Description:** Descriptive Analysis of Occupational Health and Safety Policy for Compliance and Optimization

**Project Title:** Understanding Health and Safety Policies in University Canada West

**Objective:** The main purpose of this project is to make a quantitative and qualitative investigation on the OHS data of UCW to bring out the strengths, weaknesses, opportunities and threats of the OHS in employees, and possible suggestions for its enhancement.

**Dataset:** The dataset will be derived from chatgpt, including the following information:

**Incident_Date:** Time of occurrence of the particular event.
**Incident_Type**: Categorisation of the event (for instance Near Miss, Injury or Illness).
**Worker ID:** General identifier of the worker which was effected by the occurrence.
**Report_ID:** General identifier of the report
**Report_Submission_Date:** Time report was submitted 


**Methodology:**

**Data Collection and Preparation:**

**Data Extraction:** Relevant data has to be obtained from Chatgpt.The excel downloaded should then be uploaded into the Amazon S3 bucket hr-acc-raw-swa.t (hr-acc-raw-swa).
**Data Cleaning and Data Profiling:** For data cleaning and data profiling I made project in AWS Glue Databrew . This could be via automatic connectors provided with the kit, or writing scripts by hand.With regards to Data cleaning, perform descriptive statistics and eliminate the missing values, and outliers in the Profiling step.Deliver the extracted information in a useable for analysis form, and save the information to the different bucket (hr-acc-trf-swa).
**Descrptive Statistics:**
Using AWS Glue DataBrew we can identify 
-Total of all the incidents that are recorded in the observation chart.
-Discover what types of cases are most often reported.
-Document periodic variations in the rate of occurrence of incidents.

**Data Enriching:** To load the structured data from the above mentioned worked set into amazon dynamodb for data enriching (hr-acc-appelmah-swa).

![image](https://github.com/user-attachments/assets/a127591e-8baa-4685-8939-109f51ff9459)

**Data Exploration and Analysis:** In the next process, Amazon Athena was utilized as a tool to extract data by querying from DynamoDB.

**Insights and Findings:**
-All the accident reports were filed within one day, which shows that reporting in their organization is effective.
-The dataset includes three types of accidents:
      -Slip and Fall
      -Equipment Malfunction
      -Exposure to Chemicals
This variety indicates the need for safety practices in various segments of operations.
-SOME of the accidents took place in January, March and May although due to small sample size it is difficult to infer seasonal differences.

**Recommendations:**
**Safety Training:** Provide specific training sessions to correspond to all frequent types of accidents that occur on the workplace, for instance, falling, equipment utilization, and chemical use.
**Incident Analysis:** That way, efforts to understand the causes of these accidents in order to prevent them will be worthwhile.
**Expand Data Collection:** Delay the use of the system for sometime and collect more data to be used in analyzing for trends and period which most patients are vulnerable.

**Tools and Techniques:**
**Amazon S3**: For storing the data extracted.
**AWS Glue DataBrew:** To pre-processed data from the excel sheet and convert it into standard format like CSV and then store the data in some data storage service.
**Amazon DynamoDB:** For storing the structured data where it is required to be easily queried as described in Table 1.
**Amazon Athena:** To filter the returned results of DynamoDB and to get the related stats.

**Deliverables:**
-The detailed report that contains the description of the analysis methods, results, and conclusions.
-Dashboards and visualizations are enabled through interaction using AWS tools. 
-A presentation is made to disseminate the outcome and suggestion of the research to the stakeholders.

      This descriptive analysis leverages AWS services to efficiently analyze the occupational health and safety data, providing valuable insights to improve workplace safety at UCW.


      
      
