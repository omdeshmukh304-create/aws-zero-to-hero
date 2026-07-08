# 🌐 Day 5 – AWS VPC, VPC Peering & CloudWatch

Welcome to **Day 5** of my **7 Days of AWS Challenge** 🚀

Today I explored the fundamentals of AWS networking by creating multiple Virtual Private Clouds (VPCs), configuring networking components, establishing secure communication using VPC Peering, and implementing monitoring with Amazon CloudWatch.

---

# 🎯 Objectives

- Understand AWS Virtual Private Cloud (VPC)
- Create Public Subnets
- Configure Internet Gateways
- Configure Route Tables
- Establish VPC Peering
- Verify connectivity between VPCs
- Create CloudWatch Alarm
- Configure Amazon SNS for notifications

---

# 🏗️ Architecture

📸 **Architecture Diagram**

---

# 🛠️ Services Used

- Amazon VPC
- Public Subnet
- Internet Gateway
- Route Table
- VPC Peering
- Amazon EC2
- Amazon CloudWatch
- Amazon SNS

---

# 📸 Implementation Steps

## Step 1 – Create Production VPC

Created a VPC named **Day5-prod-vpc** with its own CIDR block.

![alt text](<WhatsApp Image 2026-07-08 at 1.11.42 PM.jpeg>)

---

## Step 2 – Create Test VPC

Created another VPC named **Day5-test-vpc** for testing communication.

![alt text](<WhatsApp Image 2026-07-08 at 1.11.41 PM.jpeg>)

---

## Step 3 – Create Public Subnets

Created public subnets inside both VPCs.

![alt text](<WhatsApp Image 2026-07-08 at 1.11.41 PM (1).jpeg>)

---

## Step 4 – Create Internet Gateways

Created and attached Internet Gateways to both VPCs.

![alt text](<WhatsApp Image 2026-07-08 at 1.11.41 PM (2).jpeg>)

---

## Step 5 – Configure Route Tables

Created Route Tables and associated them with their respective public subnets.

![alt text](<WhatsApp Image 2026-07-08 at 1.11.41 PM (3).jpeg>)

---

## Step 6 – Create VPC Peering Connection

Created a VPC Peering Connection between the Production and Test VPCs and accepted the request.

![alt text](<WhatsApp Image 2026-07-08 at 1.11.40 PM.jpeg>)

---

## Step 7 – Update Route Tables

Added routes in both Route Tables to allow communication through the VPC Peering connection.

![alt text](<WhatsApp Image 2026-07-08 at 1.11.50 PM (3).jpeg>)


---

## Step 8 – Launch EC2 Instances

Launched EC2 instances in both VPCs for connectivity testing.

![alt text](<WhatsApp Image 2026-07-08 at 1.11.50 PM (2).jpeg>)


---

## Step 9 – Test Connectivity

Verified successful communication by pinging between both EC2 instances through private IP addresses.

![alt text](<WhatsApp Image 2026-07-08 at 1.11.50 PM (1).jpeg>)


---

## Step 10 – Create CloudWatch Alarm

Created a CloudWatch Alarm to monitor AWS Estimated Charges.

Threshold configured:
- Greater than or Equal to **10 USD**

![alt text](<WhatsApp Image 2026-07-08 at 1.11.51 PM.jpeg>)


---

## Step 11 – Configure SNS Topic

Created an Amazon SNS Topic to receive alarm notifications.

![alt text](<WhatsApp Image 2026-07-08 at 1.11.50 PM.jpeg>)
---
![alt text](<WhatsApp Image 2026-07-08 at 1.11.51 PM (2).jpeg>)

---

# ✅ Outcome

Successfully created two isolated VPCs, configured networking components, established secure communication using VPC Peering, verified connectivity using EC2 instances, and configured CloudWatch with SNS notifications for monitoring.

---

# 📚 Key Learnings

- AWS VPC fundamentals
- Public Subnets
- Internet Gateway
- Route Tables
- VPC Peering
- EC2 networking
- Private IP communication
- Amazon CloudWatch
- Amazon SNS
- AWS Networking Best Practices

---

# 🎯 Conclusion

Day 5 provided hands-on experience with AWS networking by designing secure cloud infrastructure, connecting isolated VPCs using VPC Peering, and implementing monitoring with Amazon CloudWatch and SNS. This lab strengthened my understanding of cloud networking concepts and resource monitoring in AWS.

---
