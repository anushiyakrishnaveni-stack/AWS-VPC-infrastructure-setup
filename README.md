# AWS VPC Infrastructure Setup: project-vpc

## 📌 Overview
This project demonstrates the creation of a custom **Amazon Virtual Private Cloud (VPC)** architecture designed for secure and scalable application deployment. Using the AWS Management Console's VPC Wizard, I provisioned a complete networking stack including subnets, routing, and gateway endpoints.

## 🎯 Purpose
The primary goal of this project was to establish a secure, isolated network environment in the **ap-southeast-2 (Sydney)** region. This infrastructure serves as the foundation for hosting web servers and databases while ensuring private connectivity to AWS services like S3 without leaving the Amazon network.

## 🏗️ Architecture Details
* **VPC ID:** `vpc-09e1410f6570015f9`
* **CIDR Block:** `10.0.0.0/16`
* **Availability Zones:** Multi-AZ deployment for fault tolerance.
* **Networking Components:**
    * **4 Subnets:** Balanced between public and private tiers.
    * **Internet Gateway (IGW):** `igw-06e67a178298a8b1e` for external traffic.
    * **VPC S3 Endpoint:** `vpce-0ca98da2abb009760` (Gateway type) to optimize S3 traffic and security.
    * **Route Tables:** 4 distinct tables associated with subnets to control ingress/egress.

## 🚀 Key Features Implemented
1.  **DNS Support:** Enabled DNS Hostnames and Resolution for easier resource identification.
2.  **S3 Integration:** Automated association of S3 endpoints with private subnet route tables.
3.  **Resource Mapping:** Visual verification of the relationship between the VPC, subnets, and route tables.

## 🧠 Lessons Learned
* Understanding the flow of traffic through Route Tables.
* The importance of VPC Endpoints in reducing data transfer costs and increasing security.
* Visualizing infrastructure through the AWS Resource Map.
