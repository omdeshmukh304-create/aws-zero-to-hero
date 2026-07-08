# 🐳 Day 6 – AWS ECS, ECR, Route 53 & CloudFront

## 📅 Date
08 July 2026

## 🎯 Objective
Learn how to deploy containerized applications using Amazon ECS and Amazon ECR, understand CloudFront for content delivery, and explore Route 53 for DNS management.

---

# 🛠️ Hands-on Lab 1 – Amazon ECR

## Step 1 – Build Docker Image

Built the Node.js Todo application Docker image locally.

![alt text](<WhatsApp Image 2026-07-08 at 11.53.36 PM (1).jpeg>)

---

## Step 2 – Create Amazon ECR Repository

Created a new Amazon Elastic Container Registry (ECR) Public Repository to store the Docker image.

![alt text](<WhatsApp Image 2026-07-09 at 12.03.25 AM.jpeg>)

---

## Step 3 – Push Docker Image to ECR

Tagged and pushed the Docker image successfully to the ECR repository.

![alt text](<WhatsApp Image 2026-07-09 at 12.05.25 AM.jpeg>)

---

# 🚀 Hands-on Lab 2 – Amazon ECS

## Step 4 – Create ECS Cluster

Created an Amazon ECS Cluster using the Fargate launch type.

![alt text](<WhatsApp Image 2026-07-09 at 12.06.10 AM.jpeg>)

---

## Step 5 – Create ECS Task Definition

Created an ECS Task Definition by specifying the container image, CPU, memory, networking, and logging configuration.

![alt text](<WhatsApp Image 2026-07-09 at 12.06.35 AM.jpeg>)

---

## Step 6 – Create ECS Service

Created an ECS Service to manage and maintain the desired number of running tasks.

![alt text](<WhatsApp Image 2026-07-09 at 12.07.29 AM.jpeg>)

---

## Step 7 – Verify Running Task

Verified that the ECS Task was successfully deployed and running.

![alt text](<WhatsApp Image 2026-07-09 at 12.07.29 AM-1.jpeg>)
---

## Step 8 – Configure CloudWatch Logs

Configured Amazon CloudWatch Logs for container monitoring and log collection.

![alt text](<WhatsApp Image 2026-07-09 at 12.08.47 AM.jpeg>)

---

## Step 9 – Verify Application

Accessed the deployed Todo application through the public endpoint and confirmed it was working successfully.

![alt text](<WhatsApp Image 2026-07-09 at 12.09.25 AM.jpeg>)

---

# 🌍 Theory – Amazon Route 53

## What is Route 53?

Amazon Route 53 is AWS's scalable Domain Name System (DNS) service used for:

- Domain Registration
- DNS Routing
- Health Checks
- Traffic Management

### DNS Flow

1. User enters a domain name.
2. DNS Resolver receives the request.
3. Root DNS Server is queried.
4. Top-Level Domain (TLD) server responds.
5. Route 53 returns the correct IP Address.
6. Browser connects to the application.

---

# ⚡ Theory – Amazon CloudFront

Amazon CloudFront is AWS's global Content Delivery Network (CDN).

### Benefits

- Low latency
- Faster content delivery
- Global Edge Locations
- HTTPS Support
- Improved Security
- Content Caching

---

# 📚 AWS Services Learned

- Amazon ECS
- Amazon ECR
- Amazon CloudWatch
- Amazon Route 53
- Amazon CloudFront

---

Successfully completed Day 6 of the 7 Days of AWS Challenge by deploying a containerized Node.js Todo application using Amazon ECS and ECR while gaining practical knowledge of CloudWatch, Route 53, and CloudFront.