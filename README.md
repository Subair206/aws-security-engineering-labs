# AWS Security Engineering Labs

Hands-on AWS security engineering projects focused on identity security, least privilege, threat detection, cloud monitoring, and security automation.

This repository documents practical AWS security exercises designed to build real-world cloud security engineering skills through implementation, testing, and validation.

---

## Objectives

- Build hands-on AWS security engineering experience
- Develop cloud identity and access management skills
- Practice security validation and authorization testing
- Learn AWS security monitoring and detection services
- Create a public portfolio demonstrating security engineering capabilities

---

# Technologies

- AWS IAM
- AWS Organizations
- MFA
- AWS CLI
- Python
- CloudTrail
- GuardDuty
- Security Hub
- EC2
- S3
- VPC

---

# Completed Labs

## Week 1: IAM Core Security

### Overview

This lab focused on implementing Identity and Access Management (IAM) security controls using AWS best practices.

The objective was to create a least-privilege environment where security analysts could investigate cloud resources without having administrative access to modify infrastructure.

---

### Skills Demonstrated

- Identity and Access Management (IAM)
- Principle of Least Privilege
- Role-Based Access Control (RBAC)
- IAM Policy Design
- Permission Validation
- Security Testing
- Multi-Factor Authentication (MFA)

---

### Components Built

#### IAM Users

Created separate users for administrative and analyst functions.

#### IAM Groups

Implemented group-based permission management.

#### IAM Roles

Configured security-focused IAM roles with scoped permissions.

#### Custom IAM Policies

Created a custom read-only security analyst policy allowing visibility into cloud resources while restricting privileged actions.

Policy file:

```text
week1-iam-core-security/iam-security-analyst-readonly-policy.json
```

#### Multi-Factor Authentication

Enabled MFA to strengthen account security and reduce credential compromise risk.

---

### Authorization Testing

After creating the custom security analyst role, validation testing was performed to ensure permissions were functioning as intended.

The following administrative actions were successfully blocked:

#### Create IAM Users

Security analysts cannot create privileged identities.

![Create IAM User Denied](screenshots/access-denied-create-iam-user.png)

---

#### Delete IAM Users

Security analysts cannot remove identities.

![Delete IAM User Denied](screenshots/access-denied-delete-iam-user.png)

---

#### Launch EC2 Instances

Security analysts cannot provision compute resources.

![Launch EC2 Denied](screenshots/access-denied-launch-ec2.png)

---

#### Create S3 Buckets

Security analysts cannot create storage resources.

![Create S3 Bucket Denied](screenshots/access-denied-create-s3-bucket.png)

---

#### Security Analyst Role

Custom least-privilege role configuration.

![Security Analyst Role](screenshots/security-admin-role.png)

---

### Security Concepts Demonstrated

#### Principle of Least Privilege

Users are granted only the permissions required to perform their job functions.

#### Role-Based Access Control (RBAC)

Permissions are assigned through roles rather than directly to users.

#### Separation of Duties

Security analysts can investigate activity but cannot make infrastructure changes.

#### Defense in Depth

MFA and restricted permissions reduce the impact of credential compromise.

#### Authorization Validation

Permissions were verified through positive and negative testing scenarios.

---

### Key Takeaways

- Learned how AWS evaluates IAM permissions.
- Practiced implementing least-privilege access models.
- Validated permission boundaries through security testing.
- Gained hands-on experience with IAM roles, policies, and MFA.
- Developed foundational cloud security engineering skills.

---

# Upcoming Labs

## Week 2: Logging & Threat Detection

Planned topics:

- AWS CloudTrail
- AWS GuardDuty
- AWS Security Hub
- Security Findings Investigation

---

## Week 3: S3 Security

Planned topics:

- Bucket Policies
- Encryption
- Public Access Controls
- Data Protection

---

## Week 4: EC2 & Network Security

Planned topics:

- Security Groups
- Network ACLs
- VPC Fundamentals
- Network Segmentation

---

## Week 5: Incident Detection & Response

Planned topics:

- Threat Detection
- Security Investigations
- Incident Response Workflows
- Security Findings Analysis

---

## Week 6: Security Automation

Planned topics:

- AWS CLI
- Python Automation
- Infrastructure as Code
- Security Operations Automation

---

# Repository Structure

```text
aws-security-engineering-labs/
│
├── week1-iam-core-security/
│   ├── screenshots/
│   │   ├── access-denied-create-iam-user.png
│   │   ├── access-denied-create-s3-bucket.png
│   │   ├── access-denied-delete-iam-user.png
│   │   ├── access-denied-launch-ec2.png
│   │   └── security-admin-role.png
│   │
│   ├── iam-security-analyst-readonly-policy.json
│   └── README.md
│
└── README.md
```

---

# Author

**Subair Dirie**

Security Analyst | IAM | Cloud Security | Security Engineering

GitHub: https://github.com/Subair206

---

# Disclaimer

This repository is intended for educational and portfolio purposes. All exercises were performed in personal AWS environments and do not contain production credentials, customer data, or proprietary information.
