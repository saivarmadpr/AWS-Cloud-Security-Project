# AWS-Cloud-Security-Project
An AWS project showcasing the design and implementation of secure AWS cloud infrastructure. Includes VPC setup, Security Groups, IAM configurations, and advanced security features like AWS WAF, GuardDuty, and Security Hub. Features automation via CloudFormation and follows AWS security best practices.

## Overview
**SecureCloud** is a project focused on designing, implementing, and managing a secure cloud environment using Amazon Web Services (AWS). The project demonstrates advanced security configurations, threat detection, and automated incident response mechanisms through real-world simulations.

---

## Features
- **Secure Architecture**: Multi-tier setup with Virtual Private Cloud (VPC), public/private subnets, and encrypted communication.
- **Identity and Access Management (IAM)**: Least-privilege roles, MFA enforcement, and secure access policies.
- **Data Protection**: End-to-end encryption for S3 buckets and RDS instances, lifecycle policies, and restricted access configurations.
- **Threat Detection**: Real-time monitoring with GuardDuty, AWS Security Hub, and vulnerability scanning using Amazon Inspector.
- **Incident Response**: Automated responses using AWS Lambda for compromised resources and malicious activity.
- **Logging & Monitoring**: Centralized logging with AWS CloudTrail, CloudWatch, and AWS Config for compliance tracking and threat analysis.
- **Simulated Attacks**: Demonstrations of S3 data breaches, EC2 compromises, and SQL injection mitigation using WAF rules.

---

## Repository Structure
```
SecureCloud/
├── README.md               # Project overview and setup instructions
├── architecture-diagrams/  # Visualizations of the AWS setup
├── cloudformation/         # AWS CloudFormation templates for IaC
├── lambda-functions/       # Code for automated incident responses
├── s3-lifecycle-policies/  # Configuration files for S3 lifecycle policies
├── logging-configs/        # CloudTrail, CloudWatch, and Config setups
├── incident-simulations/   # Scripts for simulating security incidents
├── security-reports/       # Reports on threats detected and mitigations applied
├── demo-video/             # Walkthrough video of the implementation
└── LICENSE                 # Repository license
```

---

## Objectives
- Create a secure Virtual Private Cloud (VPC).
- Configure public and private subnets.
- Set up route tables with an Internet Gateway (IGW) and NAT Gateway.

## Architecture Diagram
![VPC Diagram](https://github.com/saivarmadpr/AWS-Cloud-Security-Project/blob/da2a012f44ccad2a4f123416aa2eb1063540c45f/Diagrams/AWS_Infrastructure.drawio.png)

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

## Contributing
Contributions are welcome! Please fork the repository and submit a pull request with your changes or improvements.

---

## License
This project is licensed under the MIT License. See the `LICENSE` file for details.

---

## Contact
For questions or support, feel free to contact:
- **Sai Varma Dantuluri**: [saivarmadpr7@gmail.com](mailto:your-email@example.com)
- [GitHub Issues](https://github.com/saivarmadpr/AWS-Cloud-Security-Project/issues)

---

Enjoy building your secure AWS environment! 🚀
