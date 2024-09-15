<h1 align="center">Project 1 for AWS Assignemnt</h1>
<p align="center">
Satya Harshith Nagumothu [2221973] <br>
University Canada West<br>
BUSI 653, Section 04<br>
Instructor: Mahmood Mortazavi Dehkordi<br>
</p>

___

# Project Description: Descriptive Analysis of Lost and Found Animal Records
In this assignment I show how i designed a Data Analytic Platform (DAP) and implemented it for the City of Vancouver project, i will also explain the datasets used and the various derivations and DAP design using the datasets I selected. I got my datasets from website [City of Vancouver Open Data Portal](https://opendata.vancouver.ca/explore/dataset/issued-building-permits/information/) related to the Vancouver City operations.

## Project Title: Understanding Building Permits Issued Percentages
The primary goal here is to conduct a descriptive analysis of the yearly trends in Building permits issued based on the datasets taken from [City of Vancouver Open Data Portal](https://opendata.vancouver.ca/explore/dataset/issued-building-permits/information/). I am planning to find the percentages of permits issued for each category or type over time, which can help inform operational strategies for see the probability of getting a permit.
## Project Objective:
* Design a dAP for Building Permits Issed using Building Permits Dataset.
* I decided this will be my dataset to get information related to percentages of permits issued for each category or type over time in city of Vancouver.
* The 11 steps of information is shown below: <br>
## Datasets
* There are two datasets which I used are .
* The first dataset is **"cummulative_issued-building-permits-2024"**, it contains information on all building permits issued:
  * [cummulative_issued-building-permits 2024.xlsx](https://github.com/user-attachments/files/17004724/cummulative_issued-building-permits.2024.xlsx) contains the information of all building permits issued.
* The second datset is **"Approved-issued-building-permits-2024"**, it Contains details on approved building permits issued:
  * [Approved-issued-building-permits-2024.xlsx](https://github.com/user-attachments/files/17004726/Approved-issued-building-permits-2024.xlsx) contains the information of approved building permits issued.
* Using both these datasets I will be planning my DAP for City of Vancouver.
## Methodology:
* I will explain the process of designing the DAP below for Buildign Permits of City of vancouver:
### Step 1 - Data Analytical Question Formulation
* Data or Datasets are very important when we are going to analyse something. Similarly for me to implement DAP I need some datasets and metrics to calculate.
* As explained above I have the Issued building permits Dataset, using this am going to design my DAP. The first step is to carefully select all the relevant metrics.
* Below displayed are a few sample metrics I selected: <br>
![satya](https://github.com/user-attachments/assets/f4e65b96-e2bd-4d63-b67b-cee573d7471c)
*  From this list I am going to select the descriptive metric “What is the percentage of Permits issued for ech type of work?” analysis.
*  By doing this we can understand the total number of permits issued for each category of work.
### Step 2 - Data Discovery
* This is the dataset I gathered related to etric i selected.
* I also divided this into two, just like I explained int he Datasets section prior.
  * [cummulative_issued-building-permits 2024.xlsx](https://github.com/user-attachments/files/17004724/cummulative_issued-building-permits.2024.xlsx) contains the information of all building permits issued.
  * [Approved-issued-building-permits-2024.xlsx](https://github.com/user-attachments/files/17004726/Approved-issued-building-permits-2024.xlsx) contains the information of approved building permits issued.
 ### Step 3 - Data Storage Design
* This phase is important for the data analytic platform, where data is stored securely in the storage services provided by S3, redshift, Dynamo DB, etc, depending on the data structure.
* Amazon S3 is the ideal storage service for storing large volumes of data by providing availability, durability, and scalability, and all these features make it a preferred choice.
* I have utilized S3 Simple storage services for storing our clean and robust data for analysis purposes, as S3 offers sufficient scalability and availability and is cost-effective.
### Step 4: Dataset Preparation
* The 'Preparation' portion of the DAP process involves using the 'Microsoft Excel' service.
* This is because we cannot guarantee that the datasets we obtained are formatted in accordance with our requirements.
* To guarantee data is presentable, we need to take certain activities.
* Once the datasets are prepared, we can ensure that they can be used to improve the design and efficiency of DAP.
### Step 5: Data Ingestion & Step 6: Data Storage
* Here we create appropriate Bucket structure mentioned in Step 3.
* We can then move to uploading the dataset files into AWS environment of S3 buckets.
* This will allow ease of access to data sets in AWS environment.<br>
![figure 08](https://github.com/user-attachments/assets/076345fb-6dd9-4d26-a9c0-5fe32b53e3d5)
*The above image display “storage” for “Dataset” using ‘AWS-S3’<br>
### Step 7: Data Pipeline Design 
* The required datasets are now available on AWS. The ETL pipeline design can now begin.
* We can precisely define the data flow, from raw dataset entry to reports or ultimate outcomes.
* This stage focusses solely on the ETL pipeline implementation algorithm.
* This will provide a visual representation of how data flows through the ETL pipeline to get the desired results.<br>
![appx001](https://github.com/user-attachments/assets/63eaf976-1ccd-45fd-afcc-ef4accc1652c)
* The above image display the details of “Issued Buildign Permits” ETL process.
### Steps 8 & 9: Data Cleaning & Data Structuring
* Data cleaning included converting columns to the proper schema format and maintaining consistency amongst datasets.
* We also need to confirm that there are no missing or incomplete records by examining the datasets for analytical accuracy.
* For this, we will use the **"AWS DataBrew"** service. ,br.
![figure 22](https://github.com/user-attachments/assets/10cf90b5-ec4f-4027-afbf-1fabf3efeb48)
* The above image display the details of “Schema Information” for “**cummulative_issued-building-permits-2024**” using ‘AWS-DataBrew’.
### Step 10: Data Pipeline Implementation 
* Once our datasets have been cleansed and organised, we can start implementing the ETL pipelines created in "Step 7".
* The "**AWS Glue**" service will be utilised to implement the ETL.
* This solution converts structured data from operational sources into analytical data for specific uses.
* We can develop a schema for our datasets, an ETL job to execute the design, and an ETL pipeline diagram using "AWS Glue" components.
* If necessary, we may even guarantee that the outcome of the ETL operation is saved in our "AWS-S3."<br>
![figure 28](https://github.com/user-attachments/assets/69993e09-479d-4922-8e0f-545f5572b0ec)
* The above image display the details of “ETL information” for my dataset using ‘AWS-Glue’.
### Step 11: Data Analysis 
* Analytical datasets for our operational datasets are now available.
* The ETL pipeline's structural datasets are now available for study.
* Using the ETL results, we can create a query service with the "**AWS-Athena**" service.
* This service allows us to create tables and then retrieve data from them using simple SQL queries.<br>
![figure 32](https://github.com/user-attachments/assets/ad71ae7a-e4d0-4108-8123-636ca41e9102)
* The above image display the details of “Table” for my dataset using ‘AWS-Athena’.
* Once the results are generated based on our query we can use the resultant data by downloading it as a **".csv"** file.
### Step 12: Data Visualization 
* In this step I used "Microsoft Excel" to create reports of the **".csv"** file downloaded from AWS-Athena in "Step 11".
* My resultant reports were generated as below:<br>
![figure 36](https://github.com/user-attachments/assets/338a4dff-cb64-44a5-8c4b-6ea6e14cc621)
* The above image display the details of AWS-Athena based report using ‘Excel’.
### Step 13: Data Publishing
* This is the crucial step for populating the needed data for both internal and external use.
* We can use the ***Web servers*** and ***General Servers*** for publishing the results and making them available.
## Tools and Technologies:
* The list of Tools or technologies used are:
  * Microsoft Excel
  * AWS-S3
  * AWS-DataBrew
  * AWS-Glue
  * AWS-Athena
  * AWS-EC2
  * Microsoft Web Server IIS Role Installation
### Deliverables:
* A few crucial deliverables are:
  * **Data Analytic Platform:** Implemented on AWS, integrating data from the City of Vancouver's building permit records.
  * **Visualizations & Reports:** Generated reports and visualizations in Excel, illustrating trends, match rates, and other key findings.
  * **Data Storage & Pipeline:** Utilized AWS S3 for storage, AWS Glue for ETL processes, and AWS Athena for querying.
  * **Documentation:** Detailed steps and methodology used in the DAP design, including data preparation, cleaning, and monitoring.
  * **Recommendations:** Suggestions for improving public awareness, reporting processes, and resource allocation based on the analysis. <br>
