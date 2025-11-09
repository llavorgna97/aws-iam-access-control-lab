# AWS IAM Access Control Lab

A hands-on project demonstrating how to use AWS IAM to control access and permissions in an AWS account. This project was completed as part of my learning journey with NextWork (nextwork.org) to understand cloud security fundamentals.

---

## Project Overview

This project focuses on managing AWS access using IAM components such as users, groups, policies, and tags.  
The goal was to learn how to restrict or allow actions in development and production environments safely.

---

## Tools & Services Used

- **EC2 Instances**: Development and Production servers  
- **IAM Users**: Individual AWS identities  
- **IAM User Groups**: Grouping of users for applying shared permissions  
- **IAM Policies (Custom JSON)**: Rules defining allowed and denied actions  
- **Account Alias**: Custom AWS login URL  
- **Tags**: Used to label resources (`Key: environment`, `Value: production/development`)

---

## IAM Policies

The custom policy I created:

- Full access to development instances  
- View-only access to all instances  
- Deny creating/deleting tags  
- Deny modifying/stopping production instances  

**Key policy elements**:

- **Effect**: Allow or Deny  
- **Action**: What actions are permitted  
- **Resource**: AWS resources affected

---

## Users and Groups

- **IAM Users**: Entities who can log in to AWS  
- **IAM Groups**: Apply permissions to multiple users at once  
- The policy was attached to a group, so all users in that group inherit the permissions automatically.
