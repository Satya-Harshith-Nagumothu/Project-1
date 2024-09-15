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
* Data cleaning involved converting the columns into desired schema format and ensuring consistency between the two datasets.
* We also need to ensure the Missing or incomplete records by reviewing the datasets for accuracy of analysis.
* For this we are going to use the **"AWS DataBrew"** service.
* AWS-DataBrew helps in formatting, handling missing values, schema changes and other data cleaning and structuring tasks.<br>
 ![image](https://github.com/user-attachments/assets/95ecfd16-db46-4427-893d-bb64ed76507a)
* The above image display the details of “Schema Information” for “**Found Inventory Dataset**” using ‘AWS-DataBrew’.<br>
![image](https://github.com/user-attachments/assets/09b68971-8a03-45b0-80a1-f5ce49e5812f)
Note: The above image display the details of “Schema Information” for “**Matched Inquiries Dataset**” using ‘AWS-DataBrew’.
### Step 10: Data Pipeline Implementation 
* We can begin putting the ETL pipelines created in "Step 7" into practice after our datasets have been cleansed and organized.
* The "**AWS Glue**" service will be used for the ETL implementation.
* With the help of this service, we may transform operational data sources' structured data into the appropriate analytical data source for our purposes.
* We may provide the schema we want for our datasets, create an ETL job to carry out the entire design, and create an ETL pipeline diagram utilizing the components that "AWS Glue" offers.
* If necessary, we may even guarantee that the result of the ETL operation is stored in our "AWS-S3."<br>
![figure 31](https://github.com/user-attachments/assets/a7283be8-16ce-48dd-bf2d-645f797a5b6b)
* The above image display the details of “ETL information” for my dataset using ‘AWS-Glue’.
### Step 11: Data Analysis 
* The analytical datasets for the operational datasets we utilized are now available.
* The structural datasets produced by the ETL pipeline are now available for use in the analysis.
* On the basis of the ETL outputs, we can even build a query service using the "**AWS-Athena**" service.
* We may build tables with this service, and then use straightforward SQL queries to get the necessary data from the tables.<br>
![figure 35](https://github.com/user-attachments/assets/96511e74-41e7-4947-bfeb-9877c6436ab5)
* The above image display the details of “Table” for my dataset using ‘AWS-Athena’.
* Once the results are generated based on our query we can use the resultant data by downloading it as a **".csv"** file.
### Step 12: Data Visualization 
* In this step I used "Microsoft Excel" to create reports of the **".csv"** file downloaded from AWS-Athena in "Step 11".
* My resultant reports were generated as below:<br>
![figure 39](https://github.com/user-attachments/assets/2af9f061-94f8-4755-9fed-6137e6bebbf3)
* The above image display the details of AWS-Athena based report using ‘Excel’.
### Step 13: Data Publishing
* This is the crucial step for populating the needed data for both internal and external use.
* We can use the ***Web servers*** and ***General Servers*** for publishing the results and making them available.<br>
![figure 42](https://github.com/user-attachments/assets/0e4638ce-b264-4795-8879-0624b7bc8190)
* The above image display the details of “**IIS Role Installation**” of “**Web Server 1**”.<br>
![figure 43](https://github.com/user-attachments/assets/c2d42233-26cc-47d7-a9e2-f9ca0f108548)
* The above image display the details of “**Reports Data**” of “**Web Server 1**”.<br>
![figure 46](https://github.com/user-attachments/assets/8b1b89f3-b298-4349-9052-dabef4e7ec04)
* The above image display the details of “**Reports Data**” of “**General Server 1**”.
## Insights and Findings:
* The DAP designed can be used for other details as well.
* Below are a few finding we can use from the dataset I selected in the DAP process.
  * **Yearly Trends:** The analysis highlighted peaks in the number of lost animals around specific months or events.
  * **Matched vs. Lost Percentage:** A significant portion of lost animals (X%) were successfully matched, but Y% remained lost by the end of the year.
  * **Breed and Color Trends:** Certain breeds and colors were more commonly found or lost, which could assist in future identification and classification efforts.
  * **Seasonality:** Increased lost animal cases were observed during certain times of the year (e.g., holidays or weather-related events).
## Recommendations:
* Based on the analysis, below are a few recommendations:
  * **Improved Public Awareness Campaigns:** Focus on specific times of the year when lost animal cases are higher, encouraging pet owners to take preventive measures.
  * **Enhanced Reporting and Matching Process:** Implement a streamlined process to increase the percentage of matched animals, including better use of online reporting systems and social media for quicker identification.
  * **Resource Allocation:** Adjust staffing and resources during peak times when lost animals are more common to improve response time and matching effectiveness.
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
  * **Data Analytic Platform:** Implemented on AWS, integrating data from the City of Vancouver's lost and found animal records.
  * **Visualizations & Reports:** Generated reports and visualizations in Excel, illustrating trends, match rates, and other key findings.
  * **Data Storage & Pipeline:** Utilized AWS S3 for storage, AWS Glue for ETL processes, and AWS Athena for querying.
  * **Documentation:** Detailed steps and methodology used in the DAP design, including data preparation, cleaning, and monitoring.
  * **Recommendations:** Suggestions for improving public awareness, reporting processes, and resource allocation based on the analysis. <br>
#### This AWS Assignment highlights my whole process of designing a DAP for City of Vancouver.
