# AWS-Cloud-Security-Project
An AWS project showcasing the design and implementation of secure AWS cloud infrastructure. Includes VPC setup, Security Groups, IAM configurations, and advanced security features like AWS WAF, GuardDuty, and Security Hub. Features automation via CloudFormation and follows AWS security best practices.
# AWS Cloud Security Project: VPC Setup

## Overview
This project demonstrates a secure VPC setup with public and private subnets, following best practices for cloud security on AWS.

## Objectives
- Create a secure Virtual Private Cloud (VPC).
- Configure public and private subnets.
- Set up route tables with an Internet Gateway (IGW) and NAT Gateway.

## Architecture Diagram
![VPC Diagram](link-to-diagram)

## Steps
### 1. Create a VPC
- **Name**: My-VPC
- **CIDR Block**: `10.0.0.0/16`

### 2. Add Subnets
- **Public Subnet**:
  - Name: `Public-Subnet`
  - CIDR Block: `10.0.1.0/24`
- **Private Subnet**:
  - Name: `Private-Subnet`
  - CIDR Block: `10.0.2.0/24`

### 3. Configure Route Tables
#### Public Subnet
- Associated with the IGW.
- Route: `0.0.0.0/0` → IGW.

#### Private Subnet
- Associated with NAT Gateway.
- Route: `0.0.0.0/0` → NAT Gateway.

## Screenshots
![VPC Screenshot](link-to-screenshot)

## Key Learnings
- Importance of segregating public and private resources.
- How NAT Gateway ensures secure outbound internet access for private subnets.

## Next Steps
- Configure security groups and network ACLs for tighter security.

## Tools Used
- **AWS Management Console**
- **AWS CLI**

---
