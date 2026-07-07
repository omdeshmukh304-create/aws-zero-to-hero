# ☁️ Day 3 – Amazon S3, IAM & AWS CLI

> **7 Days of AWS Challenge – Day 3**  
> Learning how to securely store data, manage user permissions, and interact with AWS services using the AWS Command Line Interface.

---

# 📌 Overview

On Day 3, I explored three core AWS services that every Cloud Engineer should understand:

- 🪣 Amazon S3 (Simple Storage Service)
- 👤 AWS Identity and Access Management (IAM)
- 💻 AWS Command Line Interface (AWS CLI)

I also deployed a static website using Amazon S3, configured IAM permissions, and managed AWS resources using the CLI.

---

# 🎯 Objectives

- Create and configure an Amazon S3 bucket
- Host a static website using S3
- Configure custom error page (404)
- Create an IAM user with required permissions
- Configure AWS CLI
- Upload and synchronize files using AWS CLI
- Understand bucket policies and IAM policies

---

# 🏗️ Services Used

- Amazon S3
- AWS IAM
- AWS CLI
- EC2 (Ubuntu)

---

# 📖 What is Amazon S3?

Amazon Simple Storage Service (S3) is AWS object storage service used to store and retrieve any amount of data from anywhere.

### Features

- Highly Durable
- Scalable
- Secure
- Versioning
- Static Website Hosting
- Lifecycle Policies

### Common Use Cases

- Static Website Hosting
- Backup & Restore
- File Storage
- Media Hosting
- Data Archiving

---

# 📖 What is IAM?

AWS Identity and Access Management (IAM) helps securely control access to AWS resources.

Using IAM we can:

- Create Users
- Create Groups
- Create Roles
- Attach Policies
- Manage Permissions

---

# 📖 What is AWS CLI?

AWS CLI (Command Line Interface) allows managing AWS services directly from the terminal without using the AWS Console.

Benefits:

- Faster automation
- Easy scripting
- Infrastructure management
- DevOps friendly

---

# 🛠️ Practical Tasks Performed

---

# Task 1 — Created an Amazon S3 Bucket

Created a bucket named:

```
7-day-of-aws-with-tws
```

Bucket was configured for Static Website Hosting.

### Screenshot

```
images/s3-bucket-created.png
```

---

# Task 2 — Enabled Static Website Hosting

Configured:

- Index Document

```
index.html
```

- Error Document

```
error.html
```

Website Endpoint:

```
http://7-day-of-aws-with-tws.s3-website.us-east-2.amazonaws.com
```

### Screenshot

![alt text](<Screenshot 2026-07-04 234056.png>)

---

# Task 3 — Designed Website

Created a custom landing page containing:

- AWS Theme
- GitHub Button
- LinkedIn Button
- Personal Introduction
- Responsive Design

### Screenshot

![alt text](<Screenshot 2026-07-04 233912.png>)

---

# Task 4 — Created Custom 404 Error Page

Designed a custom error page with:

- Modern UI
- Home Button
- Friendly Error Message

Configured it as:

```
error.html
```

### Screenshot

![alt text](<Screenshot 2026-07-04 233933.png>)

---

# Task 5 — Configured Bucket Policy

Added a bucket policy to allow public read access for website files.

```json
{
  "Version":"2012-10-17",
  "Statement":[
    {
      "Sid":"PublicReadGetObject",
      "Effect":"Allow",
      "Principal":"*",
      "Action":"s3:GetObject",
      "Resource":"arn:aws:s3:::7-day-of-aws-with-tws/*"
    }
  ]
}
```

### Screenshot

![alt text](<Screenshot 2026-07-04 234122.png>)
---

# Task 6 — Created IAM User

Created a new IAM user for secure access.

User:

```
soham
```

Configured Console Login.

### Screenshot

![alt text](<Screenshot 2026-07-04 234927.png>)

---

# Task 7 — Assigned IAM Permissions

Attached AWS Managed Policies:

- AmazonS3FullAccess
- AmazonEC2ContainerRegistryFullAccess
- IAMFullAccess
- IAMUserChangePassword

### Screenshot


![alt text](<Screenshot 2026-07-04 234954.png>)


---

# Task 8 — Installed AWS CLI

Installed AWS CLI on Ubuntu EC2.

Verified installation:

```bash
aws --version
```

Configured CLI:

```bash
aws configure
```

Entered:

- Access Key
- Secret Access Key
- Region
- Output Format

---

# Task 9 — Uploaded Files Using AWS CLI

Uploaded website to S3.

```bash
aws s3 cp index.html s3://aws-static-demo/
```

---

Downloaded bucket contents.

```bash
aws s3 sync s3://aws-static-demo/ .
```

Uploaded new files.

```bash
aws s3 sync . s3://aws-static-demo/
```

### Screenshot

```
images/aws-cli-demo.png
```

---

# 📂 Bucket Objects

Uploaded files:

```
index.html
error.html
```
![alt text](<Screenshot 2026-07-05 001800.png>)
Successfully hosted on Amazon S3.



---

# 💻 AWS CLI Commands Used

Check CLI version

```bash
aws --version
```

Configure CLI

```bash
aws configure
```

Upload file

```bash
aws s3 cp index.html s3://aws-static-demo/
```

Sync bucket to local

```bash
aws s3 sync s3://aws-static-demo/ .
```

Sync local directory to S3

```bash
aws s3 sync . s3://aws-static-demo/
```

Display help

```bash
aws s3 help
```
---

# Key Learnings

- Learned how Amazon S3 stores objects.
- Hosted a static website using S3.
- Configured custom error pages.
- Understood Bucket Policies.
- Created IAM users and attached policies.
- Installed and configured AWS CLI.
- Uploaded and synchronized files using CLI.
- Learned how CLI simplifies cloud management.

---