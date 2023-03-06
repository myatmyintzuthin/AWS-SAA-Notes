pyan
## AWS Well-Architected Framework

- operational excellence
- security
- reliability
- performance efficiency
- cost optimization
- sustainability

## The security pillar

The security pillar signifies the ability to protect information, systems, and assets while delivering business value through risk assessments and mitigation strategies. 
Security pillar areas:
- Identity and Access Management
- Detective Controls
- Infrastructure Protection
- Data Protection
- Incident Response

## Identity and Access Management

**Amazon Cognito** - a service for simple user sign-up, sign-in and access control to your web and mobile apps.
**Use Case**:
An Amazon Cognito user pool is a user directory that manages the overhead of handling the tokens that are returned from social identity providers. After a successful user pool sign-in, your web or mobile app will receive user pool tokens from Amazon Cognito. These tokens can then be used to retrieve AWS credentials via Amazon Cognito identity pools. These credentials allow your app to access other AWS services, and you don’t have to embed long-term AWS credentials in your app.

![[Screenshot from 2023-03-05 16-55-53.png]]

**AWS Directory Service** - A managed service that provices directories that contain information about your organization, including users, groups, computers and other resources.
**Use Case:**
If you already have an Active Directory infrastructure and want to use it when migrating Active Directory aware workloads to the AWS Cloud, AWS Managed Microsoft AD can help. You can use Active Directory trusts to connect AWS Managed Microsoft AD to your existing Active Directory. This means your users can access Active Directory aware and AWS applications with their on-premises Active Directory credentials without needing you to synchronize users, groups, or passwords.

![[Screenshot from 2023-03-05 17-05-24.png]]

**AWS IAM** - a service that enables to securely manage access to AWS services and resources in your account. You can create users and groups and apply permissions to allow or deny access to AWS resources.

**AWS IAM Identity Center (SSO)** - IAM Identity Center includes built-in Security Assertion Markup Language (SAML) integrations to many business applications. IAM Identity Center may be integrated with Microsoft Active Directory, which means your employees can sign in to your user portal using their corporate Active Directory credentials.

## Monitoring Overview

**AWS Security Hub** - provides you with a comprehensive view of your security state within AWS and your compliance with security standards and best practices. Centralizes and prioritiizes security findings from across AWS accounts, services and supported third-party partners to help you analyze your security trends and identify the highest priority security issues.

