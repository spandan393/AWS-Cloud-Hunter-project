# 🛡️ CLOUD HUNTER PROJECT PORTFOLIO 🛡️

### Practical Cloud Security Engineering & AWS IAM Hardening

---

# AWS-Cloud-Hunter-project
Demonstrating practical AWS security hardening using IAM , S3 , and , CloudTrail.

## 1. Project: Least Privilege Enforcement

### Skill Demonstrated: IAM Policy Hardening (PoLP)

GOAL: Prevent attackers from using the dangerous wildcard '*' (full control) in an IAM role and restrict permissions to only the necessary read actions on one S3 bucket (`prod-data-secrets`).

**REQUIRED ACTIONS:** To list files: `s3:ListBucket` To download files: `s3:GetObject` 
This policy demonstrates compliance with the core AWS security principle of granting only the minimum permissions needed.

## 2. Project: Secure Cross-Account Access

### Skill Demonstrated: Trust Policy Implementation (Incident Prevention)

GOAL: Enable a role in one account (Source: 111111111111) to temporarily access resources in another account (Target: 222222222222).

CRITICAL ACTION: The Target role's Trust Policy must explicitly allow the `sts:AssumeRole` action from the Source role.

WHY THIS IS SECURE: This prevents the need to share long-lived credentials (like Access Keys) and grants only temporary, short-lived tokens, which is the industry standard for cloud access.

## 3. Project: Preventative Security Guardrails

### Skill Demonstrated: Condition Key Enforcement

This section demonstrates how to use IAM Condition Keys to enforce the highest level of security, blocking access based on how and where the user is logging in.

#### A. MFA Enforcement (Stopping Stolen Passwords) Key Condition Used: `aws:IsMultiFactorAuthPresent` Logic: Policy is set to DENY access unless this condition key is set to 'true'. This prevents access if an attacker has stolen the user's password but does not have their MFA token. 
#### B. IP Restriction (Stopping Remote Attackers) Key Condition Used: `aws:SourceIp` Logic: Policy denies access if the request does not originate from a specific, secure company IP address range (e.g., 192.168.1.0/24). This is used to lock down 

---
### 🤝 Let's Connect

Available for: Part-time, flexible, remote contract work (IAM/S3/CloudTrail Auditing)
Contact: spandhan.panta@gmail.com
Certification Progress: Actively studying for AWS Certified Security - Specialty
highly sensitive resources like admin roles.

