# 🔒 AWS WAF for Web Application Protection
## Day 2 – 7 Days of AWS Challenge

As part of **Day 2 of the 7 Days of AWS Challenge**, I learned how to secure a web application using **AWS WAF (Web Application Firewall)**. Along with implementing AWS WAF, I also built a scalable infrastructure using **Application Load Balancer (ALB)** and **Auto Scaling Group (ASG)** to improve application availability.

---

# 📌 Project Objective

The objective of this project was to:

- Deploy a scalable web application architecture.
- Configure an Application Load Balancer.
- Configure an Auto Scaling Group.
- Simulate CPU load using the `stress` utility.
- Protect the application using AWS WAF.
- Monitor incoming requests using AWS WAF.

---

# 🏗️ Architecture

The application architecture consists of:

- Internet Users
- AWS WAF
- Application Load Balancer
- Auto Scaling Group
- Amazon EC2 Instances

![alt text](<WhatsApp Image 2026-07-04 at 9.20.15 PM.jpeg>)

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

# 🚀 Part 1 – Configure Auto Scaling Infrastructure

## Step 1 – Review Auto Scaling Configuration

Configured the Auto Scaling Group using the Launch Template and attached it to the Application Load Balancer.

The following configuration was verified:

- Load Balancer
- Target Group
- Health Checks
- Desired Capacity
- Minimum Capacity
- Maximum Capacity

![alt text](<Screenshot 2026-07-04 161309.png>)

---

Configured the scaling policy to automatically launch additional EC2 instances whenever CPU utilization increases.

![alt text](<Screenshot 2026-07-04 161336.png>)

---

Reviewed notifications, tags and additional Auto Scaling settings before creating the Auto Scaling Group.

![alt text](<Screenshot 2026-07-04 161424.png>)

---

## Step 2 – Simulate High CPU Utilization

Installed the **stress** package and generated CPU load.

```bash
sudo apt update

sudo apt install stress

stress -c 70
```

This command creates high CPU utilization, allowing the Auto Scaling policy to launch additional EC2 instances when required.

![alt text](<Screenshot 2026-07-04 164518.png>)

---

# 🔒 Part 2 – Secure the Application Using AWS WAF

## Step 3 – Create a Web ACL

Opened AWS WAF & Shield and created a new **Regional Web ACL**.

Configured:

- Web ACL Name
- AWS Region
- Regional Resources

![alt text](<WhatsApp Image 2026-07-04 at 9.01.30 PM.jpeg>)
---

## Step 4 – Configure AWS Managed Rules

Added AWS Managed Rule Groups to protect the application.

Configured Rule Sets:

- AWS Core Rule Set
- Known Bad Inputs Rule Set
- SQL Injection Rule Set
- Linux Rule Set

These rules automatically inspect and block malicious requests.

![alt text](<WhatsApp Image 2026-07-04 at 9.01.31 PM.jpeg>)
---

Verified the configured Managed Rule Groups before proceeding to the next step.

![alt text](<WhatsApp Image 2026-07-04 at 9.01.30 PM (1).jpeg>)

---

## Step 5 – Associate Web ACL with Application Load Balancer

Associated the Web ACL with the existing Application Load Balancer so that every incoming HTTP request is inspected before reaching the application.

![alt text](<WhatsApp Image 2026-07-04 at 9.01.30 PM (2).jpeg>)

---

## Step 6 – Verify Web ACL Configuration

Verified:

- Web ACL Name
- Scope
- Default Action
- Associated Resource
- Capacity Units

This confirmed that AWS WAF was successfully protecting the Application Load Balancer.

![alt text](<WhatsApp Image 2026-07-04 at 9.01.29 PM.jpeg>)

---

## Step 7 – Monitor Traffic

Opened the **Logging & Metrics** dashboard to monitor:

- Total Requests
- Allowed Requests
- Blocked Requests
- Request Rate

This dashboard provides visibility into incoming traffic and blocked malicious requests.

![alt text](<WhatsApp Image 2026-07-04 at 9.01.29 PM (1).jpeg>)

---

# 🔐 Security Features

- AWS WAF
- Web ACL
- AWS Managed Rules
- SQL Injection Protection
- Cross-Site Scripting (XSS) Protection
- Bad Input Detection
- Application Load Balancer Protection
- Logging & Metrics

---

# 📈 Project Outcome

Successfully built a scalable and secure AWS architecture by combining:

- Amazon EC2
- Application Load Balancer
- Auto Scaling Group
- AWS WAF

The Auto Scaling Group automatically launches additional EC2 instances during increased CPU utilization, while AWS WAF inspects and filters incoming HTTP requests before they reach the application.

---

# 🎯 Learning Outcomes

During this hands-on project, I learned:

- How Application Load Balancer distributes incoming traffic.
- How Auto Scaling improves application availability.
- How to simulate CPU load using the `stress` utility.
- How AWS WAF protects web applications.
- How AWS Managed Rules defend against common web attacks.
- How to associate AWS WAF with an Application Load Balancer.
- How to monitor requests using AWS WAF Logging & Metrics.

---

# 📸 Screenshot Sequence

| Image | Description |
|--------|-------------|
| Image 1 | Architecture Diagram |
| Image 2 | Auto Scaling Review (Load Balancer & Group Size) |
| Image 3 | Auto Scaling Scaling Policy |
| Image 4 | Notifications & Tags |
| Image 5 | CPU Stress Test |
| Image 6 | Create Web ACL |
| Image 7 | Configure Managed Rules |
| Image 8 | Review Managed Rules |
| Image 9 | Associated AWS Resources (ALB) |
| Image 10 | Web ACL Overview |
| Image 11 | Logging & Metrics |

---

# 👨‍💻 Author

**Om Deshmukh**

Completed as part of **Day 2 – 7 Days of AWS Challenge**, where I implemented AWS WAF to secure a web application while using Auto Scaling and an Application Load Balancer to build a highly available and scalable AWS architecture.