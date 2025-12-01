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
