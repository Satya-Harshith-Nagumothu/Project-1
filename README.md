<h1 align="center">Project 1 for AWS Assignemnt</h1>
<p align="center">
Satya Harshith Nagumothu [2221973] <br>
University Canada West<br>
BUSI 653, Section 04<br>
Instructor: Mahmood Mortazavi Dehkordi<br>
</p>

___

# Project Description: Descriptive Analysis of Lost and Found Animal Records
In this assignment I will be describing the details of the City of Vancouver project mainly about the Data Analytic Platform (DAP) implementation (the datasets used and the various derivations and DAP design using the datasets I selected. For this assignment I used the website [City of Vancouver Open Data Portal](https://opendata.vancouver.ca/explore/dataset/animal-control-inventory-lost-and-found/export/?disjunctive.breed&disjunctive.color&sort=date&refine.date=2023) for getting some open source available datasets for various segments related to the Vancouver City operations.

## Project Title: Understanding Yearly Lost and Found Animal Patterns
The primary need of this project is to conduct a descriptive analysis of the yearly trends in lost and found animals based on the datasets taken from [City of Vancouver Open Data Portal](https://opendata.vancouver.ca/explore/dataset/animal-control-inventory-lost-and-found/export/?disjunctive.breed&disjunctive.color&sort=date&refine.date=2023). The goal is to identify the percentage of animals matched (found) and lost over time, which can help inform operational strategies for animal control services, improve response times, and increase the likelihood of reuniting lost animals with their owners.
## Project Objective:
* Pets have become a major part of our lives.
* I decided this will be my dataset to get information related to lost and found cases related to pets in city of Vancouver.
* For the DAP design there are close to 13 steps. Am going to define and describe all these steps below.
## Datasets
* There are two datasets wi=hich i will be using here.
* The first dataset is **"Found Inventory Dataset"**, it contains information on animals found, with columns such as:
  * SNO: Serial Number
  * Breed: Animal breed
  * Color: Color description
  * Date: Date when the animal was found
  * Name: Name of the animal
  * Sex: Animal's sex
  * State: Status (Yes indicating matched or found)
  * [2024_animal_control_Found_inventory.xlsx](https://github.com/user-attachments/files/16974871/2024_animal_control_Found_inventory.xlsx) contains the information of this match found dataset.
* The second datset is **"Lost and Found Inventory Dataset"**, it Contains details on lost animals, with similar columns, including:
  * SNO: Serial Number
  * Breed: Animal breed
  * Color: Color description
  * Date: Date of the record
  * Name: Name of the animal
  * Sex: Animal's sex
  * State: Lost or Found status
  * [2024_animal_control_inventory_lost_and_found.xlsx](https://github.com/user-attachments/files/16974850/2024_animal_control_inventory_lost_and_found.xlsx) contains the information of this lost and found inventory dataset.
* Using both these datasets I will be planning my DAP for City of Vancouver.
## Methodology:
* The process of DAP designing and implementation is complex.
* This involves close to 13 different steps. I will be explaining on these steps in detail below:
### Step 1 - Data Analytical Question Formulation
* Data or Datasets are very important when we are going to analyse something. Similarly for me to implement DAP I need some datasets and metrics to calculate.
* As explained above I have the Animal Control Inventory Lost & Found dataset, using this am going to design my DAP. The first step is to carefully select all the relevant metrics.
* Below displayed are a few sample metrics I selected:
![step001](https://github.com/user-attachments/assets/496f5579-6aed-48a2-a71e-5b83cb3c331e)
*  From this list I am going to select the descriptive metric “What is the match rate of Pet Inquiries?” analysis.
*  By doing this we can understand the total number of pet inquiries done, the number of match found inquiries, the number of inquiries still pending , and also the percentage of matched inquiries to that of total inquiries.
### Step 2 - Data Discovery
* This is the dataset I gathered pertaining to pet-related questions. The breed, color, name, gender, date of inquiry, status, and other details about pets that have been reported missing or found are all included in this dataset.
* I also divided this into two, just like I explained int he Datasets section prior.
  * [2024_animal_control_Found_inventory.xlsx](https://github.com/user-attachments/files/16974871/2024_animal_control_Found_inventory.xlsx) contains the information of this match found dataset.
  * [2024_animal_control_inventory_lost_and_found.xlsx](https://github.com/user-attachments/files/16974850/2024_animal_control_inventory_lost_and_found.xlsx) contains the information of this lost and found inventory dataset.
### Step 3 - Data Storage Design
* This phase is the backbone of the data analytic platform, where data is stored securely in the storage services provided by S3, redshift, Dynamo DB, etc, depending on the data structure. * Amazon S3 is the ideal storage service for storing large volumes of data by providing availability, durability, and scalability, and all these features make it a preferred choice.
* I have utilized S3 Simple storage services for storing our clean and robust data for analysis purposes, as S3 offers sufficient scalability and availability and is cost-effective.
* Below image displays my data storage design<br>
![step003](https://github.com/user-attachments/assets/c5b75964-cc2f-48ca-920c-3c60ea400ce0)
### Step 4: Dataset Preparation
* The next step in the DAP process, that is the ‘Preparation’ stage.
* For this we are going to use ‘Microsoft Excel’ service.
* This is because we can not be sure the datasets we took is structured as per out need.
* To ensure this we need to do set of actions to ensure the data is in presentable format.
* Once the datasets are prepared then we can ensure that we can use them to further design and efficient DAP.
### Step 5: Data Ingestion & Step 6: Data Storage
* These are the steps where we create appropriate Bucket structure mentioned in Step 3.
* Once the buckets & folders are created we can then move to uploading the dataset files into AWS environment of S3 buckets.
* This will allow ease of access to data sets in AWS environment.<br>
![image](https://github.com/user-attachments/assets/4602b53b-ee88-475d-a77f-3e830077962b)
*The above image display the details of “Storage” & "Ingestion" for “**Pet Inquiries**” of "***Lost and Found Inventory Dataset***"using ‘AWS-S3’<br>
![image](https://github.com/user-attachments/assets/bc5aa6bf-8f6c-481a-a63e-4c501c3f224f)
*The above image display the details of “Storage” & "Ingestion" for “**Matched Inquiries**” of "***Found Inventory Dataset***"using ‘AWS-S3’
### Step 7: Data Pipeline Design 
* The datasets we need are now available in the AWS environment.
* The ETL pipeline design can now be started.
* We are able to define the precise data flow, starting from the raw datasets' input and ending with the reports or final outcomes.
* The ETL pipeline implementation's algorithm is the sole thing involved in this stage. This will provide a visual depiction of how data moves through the ETL pipeline to produce the required outputs.<br>
![appx004](https://github.com/user-attachments/assets/0f36382f-7be8-4005-927a-697802f6ccfd)
* The above image display the details of “Pets Lost & Found” ETL process.
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
