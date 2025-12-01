# AWS-Cloud-Hunter-project
Demonstrating practical AWS security hardening using IAM , S3 , and , CloudTrail.

## 1. Project: Least Privilege Enforcement

### Skill Demonstrated: IAM Policy Hardening (PoLP)

GOAL: Prevent attackers from using the dangerous wildcard '*' (full control) in an IAM role and restrict permissions to only the necessary read actions on one S3 bucket (`prod-data-secrets`).

**REQUIRED ACTIONS:** To list files: `s3:ListBucket` To download files: `s3:GetObject` 
This policy demonstrates compliance with the core AWS security principle of granting only the minimum permissions needed.
