# 🔒 AWS WAF for Web Application Protection
## Day 2 – 7 Days of AWS Challenge

This project demonstrates how I built a scalable web application infrastructure using **Amazon EC2**, **Application Load Balancer (ALB)**, and **Auto Scaling Group**, then secured it with **AWS WAF (Web Application Firewall)** to protect against common web attacks.

---

# 📌 Project Objective

The objective of this project was to:

- Deploy a web application on Amazon EC2.
- Configure an Application Load Balancer.
- Implement Auto Scaling for high availability.
- Simulate high CPU usage using the `stress` tool.
- Secure the application using AWS WAF.
- Protect the application against common web attacks using AWS Managed Rules.

---

# 🏗️ Architecture

```
                    Internet
                        │
                        ▼
                  AWS WAF (Web ACL)
                        │
                        ▼
         Application Load Balancer (ALB)
                        │
                        ▼
             Auto Scaling Group (ASG)
                  │               │
                  ▼               ▼
          EC2 Instance      EC2 Instance
            (Web App)         (Scaled)
```

---

# 🛠️ AWS Services Used

- Amazon EC2
- Application Load Balancer (ALB)
- Auto Scaling Group (ASG)
- Launch Template
- AWS WAF
- AWS Managed Rule Groups
- CloudWatch
- Ubuntu Server

---

# 🚀 Implementation

## Step 1 – Launch EC2 Instance

Created an Ubuntu EC2 instance and deployed the sample web application.

### Screenshot

> 📸 **Insert your EC2 Instance screenshot here**

![alt text](<WhatsApp Image 2026-07-04 at 7.35.44 PM.jpeg>)

---

## Step 2 – Create an Application Load Balancer

Configured an Internet-facing Application Load Balancer and attached the EC2 instance through a Target Group.

### Screenshot

> 📸 **Insert your ALB screenshot here**

```
images/02-load-balancer.png
```

---

## Step 3 – Create a Launch Template

Created a Launch Template containing the AMI, instance type, security group, and key pair for Auto Scaling.

### Screenshot

> 📸 **Insert your Launch Template screenshot here**

```
images/03-launch-template.png
```

---

## Step 4 – Configure Auto Scaling Group

Configured an Auto Scaling Group with the following settings:

- Minimum Capacity: 2
- Desired Capacity: 2
- Maximum Capacity: 4

### Screenshot

> 📸 **Insert your Auto Scaling Group screenshot here**


---

## Step 5 – Simulate High CPU Utilization

Installed the **stress** package and generated CPU load to trigger the Auto Scaling policy.

```bash
sudo apt update
sudo apt install stress

stress -c 70
```

### Screenshot

> 📸 **Insert your Stress Command screenshot here**

```
images/05-stress-test.png
```

---

## Step 6 – Verify Auto Scaling

Verified that Auto Scaling automatically launched additional EC2 instances when CPU utilization increased.

### Screenshot

> 📸 **Insert your Running EC2 Instances screenshot here**

```
images/06-running-instances.png
```

---

# 🔒 AWS WAF Implementation

## Step 7 – Create a Web ACL

Opened AWS WAF and created a Regional Web ACL.

### Screenshot

> 📸 **Insert WAF Dashboard screenshot here**

```
images/07-waf-dashboard.png
```

---

## Step 8 – Configure AWS Managed Rules

Configured the following AWS Managed Rule Groups:

- AWS Core Rule Set
- Known Bad Inputs Rule Set
- SQL Database Rule Set

These rules help protect the application from:

- SQL Injection (SQLi)
- Cross-Site Scripting (XSS)
- Malicious Requests

### Screenshot

> 📸 **Insert Managed Rules screenshot here**

```
images/08-managed-rules.png
```

---

## Step 9 – Associate Web ACL with ALB

Associated the Web ACL with the existing Application Load Balancer.

### Screenshot

> 📸 **Insert Associated Resource screenshot here**

```
images/09-associated-resource.png
```

---

## Step 10 – Monitor Requests

Verified request inspection through AWS WAF Logging & Metrics.

### Screenshot

> 📸 **Insert Logging & Metrics screenshot here**

```
images/10-waf-metrics.png
```

---

# 🔐 Security Features

- AWS Managed Rules
- SQL Injection Protection
- Cross-Site Scripting (XSS) Protection
- Known Bad Inputs Detection
- Application Load Balancer Protection
- Automatic Request Inspection
- Traffic Monitoring
- Logging & Metrics

---

# 📈 Project Outcome

Successfully built a highly available and secure AWS architecture by combining:

- Amazon EC2
- Application Load Balancer
- Auto Scaling Group
- AWS WAF

The application can automatically scale during high traffic while AWS WAF inspects and filters incoming requests before they reach the backend application.

---

# 🎯 Learning Outcomes

Through this project, I learned:

- How to deploy applications on Amazon EC2.
- How Application Load Balancer distributes traffic.
- How Auto Scaling improves application availability.
- How to simulate workload using the `stress` tool.
- How AWS WAF protects web applications.
- How AWS Managed Rules defend against common web attacks.
- How to build a secure and scalable cloud architecture.

---

# 📂 Repository Structure

```
AWS-WAF-Day2/
│── README.md
│── images/
│   ├── 01-ec2-instance.png
│   ├── 02-load-balancer.png
│   ├── 03-launch-template.png
│   ├── 04-auto-scaling-group.png
│   ├── 05-stress-test.png
│   ├── 06-running-instances.png
│   ├── 07-waf-dashboard.png
│   ├── 08-managed-rules.png
│   ├── 09-associated-resource.png
│   └── 10-waf-metrics.png
```

---

# 👨‍💻 Author

**Om Deshmukh**

This project was completed as part of **Day 2 – 7 Days of AWS Challenge**, where I focused on building a scalable AWS infrastructure and securing it using **AWS WAF**.