# 🗄️ Day 4 -- Databases, Lambda & Automation

Welcome to **Day 4** of the **7 Days of AWS Challenge** 🚀

Today I explored AWS database services and serverless computing by
implementing two hands-on labs. The first focused on deploying a managed
MySQL database using **Amazon RDS** and connecting it through **Amazon
EC2**. The second demonstrated serverless data operations using **AWS
Lambda**, **Amazon DynamoDB**, and **IAM Roles**.

------------------------------------------------------------------------

# 🧠 Concepts to Learn

## 💾 Amazon RDS

Amazon RDS is a fully managed relational database service that
simplifies database deployment, backups, patching, monitoring, and
scaling.

## ⚡ Amazon DynamoDB

Amazon DynamoDB is a fully managed NoSQL database that delivers high
performance with single-digit millisecond latency.

## ⚙️ AWS Lambda

AWS Lambda is a serverless compute service that runs code in response to
events without managing servers.

## 🔐 AWS IAM

AWS IAM securely manages permissions using users, groups, roles, and
policies.

------------------------------------------------------------------------

# 🛠️ Hands-on Lab 1 -- Amazon RDS with EC2

## Step 1 -- Launch an Amazon RDS MySQL Instance

Created a MySQL database instance from the AWS Console.

![alt text](<WhatsApp Image 2026-07-07 at 10.40.17 PM.jpeg>)

## Step 2 -- Configure Database Settings

Configured database name, credentials, networking, storage, and security
groups.

![alt text](<WhatsApp Image 2026-07-07 at 10.40.16 PM.jpeg>)

## Step 3 -- Wait for Instance Availability

Verified that the RDS instance reached the **Available** state.

![alt text](<WhatsApp Image 2026-07-07 at 10.40.16 PM-1.jpeg>)

## Step 4 -- Connect to EC2

Connected to an EC2 instance using SSH.

![alt text](<WhatsApp Image 2026-07-07 at 10.40.16 PM (2).jpeg>)

## Step 5 -- Install MySQL Client

Installed the MySQL client package.

![alt text](<WhatsApp Image 2026-07-07 at 10.40.15 PM.jpeg>)

## Step 6 -- Connect to Amazon RDS

Connected to the database using the RDS endpoint.

![alt text](<WhatsApp Image 2026-07-07 at 10.40.15 PM-1.jpeg>)

## Step 7 -- Create Database & Table

Created a new database and table using SQL.

![alt text](<WhatsApp Image 2026-07-07 at 10.40.14 PM.jpeg>)

## Step 8 -- Perform SQL Operations

Inserted, queried, updated, and deleted records to verify connectivity.

![alt text](<WhatsApp Image 2026-07-07 at 10.40.14 PM (1).jpeg>)

------------------------------------------------------------------------

# 🛠️ Hands-on Lab 2 -- AWS Lambda with DynamoDB

## Step 9 -- Create DynamoDB Table

Created a table named **learners** with **learner_id** as the partition
key.

![alt text](<WhatsApp Image 2026-07-07 at 10.43.04 PM.jpeg>)

## Step 10 -- Create Lambda Function

Created a Python Lambda function for DynamoDB operations.

![alt text](<WhatsApp Image 2026-07-07 at 10.43.04 PM-1.jpeg>)

## Step 11 -- Configure IAM Role

Attached the required IAM permissions for DynamoDB access.

![alt text](<WhatsApp Image 2026-07-07 at 10.43.04 PM (2).jpeg>)

## Step 12 -- Develop Lambda Code

Implemented the insert logic using the **boto3** SDK.

![alt text](<WhatsApp Image 2026-07-07 at 10.43.03 PM.jpeg>)

## Step 13 -- Create Test Event

Prepared a JSON event with learner details.

![alt text](<WhatsApp Image 2026-07-07 at 10.43.03 PM (1).jpeg>)

## Step 14 -- Execute Lambda Function

Invoked the function and successfully inserted data into DynamoDB.

![alt text](<WhatsApp Image 2026-07-07 at 10.43.02 PM (1).jpeg>)

## Step 15 -- Verify Records

Confirmed that the records were stored in DynamoDB.

![alt text](<WhatsApp Image 2026-07-07 at 10.43.02 PM (2).jpeg>)

## Step 16 -- Delete Records using Lambda

Created another Lambda function to delete records and verified the
deletion.

![alt text](<WhatsApp Image 2026-07-07 at 10.43.02 PM (2)-1.jpeg>)

------------------------------------------------------------------------

# 🏗️ Architecture

![alt text](<ChatGPT Image Jul 7, 2026, 10_29_13 PM.png>)

------------------------------------------------------------------------

# ✅ Key Learnings

-   Deployed and configured Amazon RDS.
-   Connected EC2 with RDS.
-   Performed SQL CRUD operations.
-   Created DynamoDB tables.
-   Developed Lambda functions using Python.
-   Configured IAM Roles and Policies.
-   Performed Insert and Delete operations in DynamoDB.
-   Validated serverless workflows using Lambda Test Events.

------------------------------------------------------------------------

# 🛠️ AWS Services Used

-   Amazon EC2
-   Amazon RDS
-   Amazon DynamoDB
-   AWS Lambda
-   AWS IAM
-   Amazon CloudWatch

------------------------------------------------------------------------

# 📌 Outcome

Successfully implemented relational and NoSQL database workflows using
Amazon RDS, Amazon DynamoDB, and AWS Lambda. This lab demonstrated
secure database connectivity, serverless automation, and practical cloud
database management on AWS.
