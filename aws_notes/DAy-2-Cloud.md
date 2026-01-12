# DAY 2 – IAM (Identity & Access Management) – Detailed Interview Q&A

**1) What is IAM in AWS?**

**Answer:**
IAM (Identity and Access Management) is an AWS service that helps you securely control access to AWS resources. Using IAM, you can decide:
Who can access AWS (authentication)
What they can do (authorization)

**In simple words, IAM is used to manage:**
Users
Groups
Roles
Permissions

**Example:**
**In a company:**
Developers need access to EC2
HR team needs only billing access
DevOps team needs full access
Using IAM, you can give different permissions to different people.

**2) What is an IAM User?**

**Answer:**
An IAM user represents a person or application that interacts with AWS.
Each user has:
A username
Password (for console)
Access keys (for CLI/API)
Permissions

**Example:**
If your team has 5 developers, you should create 5 separate IAM users instead of sharing one root account.
**Why not use root account?**
Root account has full access. If compromised, everything is lost.

**3) What is an IAM Group?**

**Answer:**
An IAM group is a collection of IAM users. Instead of assigning permissions to each user individually, you assign them to a group.
**Example:**
Group: Developers
**Permissions:**
EC2 full access
S3 read-only
Now any user added to this group automatically gets these permissions.

**4) What is an IAM Role?**

**Answer:**
An IAM role is used to give temporary permissions to AWS services or users.
Roles are mostly used by:
EC2
Lambda
Cross-account access

**Example:**
An EC2 instance needs to access S3.
Instead of storing AWS keys in EC2, you attach a role with S3 permissions.

**Why roles are better than access keys?**
More secure
Temporary credentials
No hardcoding

**5) What is an IAM Policy?**

**Answer:**
An IAM policy is a JSON document that defines what actions are allowed or denied on which AWS resources.
Example Policy:
Allow EC2 start/stop:
{
  "Effect": "Allow",
  "Action": ["ec2:StartInstances", "ec2:StopInstances"],
  "Resource": "*"
}

**6) What are the types of IAM Policies?**

**Answer:**
AWS Managed Policy – Created by AWS
Example: AmazonS3FullAccess
Customer Managed Policy – Created by you
Inline Policy – Directly attached to a user

**7) What is MFA?**

**Answer:**
MFA (Multi-Factor Authentication) adds an extra layer of security.
Login requires:
Password
OTP (from phone/app)

**Example:**
Even if someone steals your password, they still can’t login without OTP.

**8) What is the Principle of Least Privilege?**

**Answer:**
Give users only the permissions they need — nothing more.

**Example:**
If a user only needs to view S3, don’t give full S3 access.

**9) Difference between IAM User and Role?**

	                
| **IAM User**          |             | **IAM Role**          |
|-----------------------|-------------|-----------------------|
| Permanent             |             | Temporary             |
| For people            |             | For services          |
| Has password          |             | No password           |
| Long-term credentials |             | Short-term credentials|

   	        

**10) What is AWS Organizations?**

**Answer:**
AWS Organizations allows you to manage multiple AWS accounts centrally.

**Example:**
**Company has:**
Dev account
Test account
Prod account
You can manage all under one organization.

**11) What is STS (Security Token Service)?**

**Answer:**
STS provides temporary security credentials for users and services.
Used in:
Cross-account access
Federation
Roles

**12) What happens if IAM is not used properly?**

**Answer:**
Security breaches
Data loss
Unauthorized access
Financial loss