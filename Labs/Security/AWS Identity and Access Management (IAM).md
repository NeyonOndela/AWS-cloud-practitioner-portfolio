## Introduction

In modern business environments, secure access to systems and resources is critical. Organizations rely on authentication and authorization mechanisms to ensure that only approved users can access sensitive information and services. Without proper access control, unauthorized users can exploit company resources such as shared folders, intranets, printers, and internal systems.

This project explores **AWS Identity and Access Management (IAM)**, a core AWS service that enables secure control of access to AWS resources. Through this lab, I gained hands-on experience in managing users, groups, and policies while understanding how access permissions are enforced within the AWS environment.



## Understanding AWS IAM

AWS Identity and Access Management (IAM) is a global AWS service that allows administrators to securely manage access to AWS resources. IAM enables the creation of users, assignment of permissions, and enforcement of security policies without sharing root account credentials.

IAM operates based on the principle of least privilege, meaning users are granted only the permissions necessary to perform their tasks. This minimizes security risks and ensures tighter control over cloud resources.



**The primary goal of this lab was to understand how IAM controls authentication and authorization in AWS. After completing the lab, I was able to:**

- Create and apply an IAM password policy

- Explore pre-created IAM users and user groups

- Inspect IAM policies applied to user groups

- Add users to groups with specific permissions

- Locate and use the IAM sign-in URL

- Test how policies affect access to AWS services



## Creating and Applying an IAM Password Policy

The first task involved configuring an IAM password policy. This policy enforces password strength requirements for all IAM users within the account.

I configured the policy to:

- Require a minimum password length

- Include uppercase and lowercase characters

- Require numbers and special characters

- Enforce password expiration

This step reinforced the importance of strong authentication mechanisms in preventing unauthorized access.

<img width ="1000" height="500" alt="instance1" src= "https://github.com/NeyonOndela/AWS-Security/blob/ef33e917ae3719db32153a3df9d337d84a0f5b09/resources/secu.jpg" />


## Exploring Pre-Created IAM Users and Groups

Next, I examined pre-created IAM users and groups. Users represent individual identities within AWS, while groups allow administrators to assign permissions collectively.By reviewing the users and groups, I observed how permissions were not assigned directly to users in most cases. Instead, permissions were attached to groups, and users inherited permissions based on group membership. This simplifies administration and improves scalability.



## Inspecting IAM Policies

IAM policies define what actions are allowed or denied on specific AWS resources. These policies are written in JSON format and specify:
- The effect (Allow or Deny)
- The actions permitted
- The resources affected

By inspecting attached policies, I learned how permissions determine access to AWS services such as EC2, S3, and others. I also observed how explicit deny statements override allow permissions.

<img width ="1000" height="500" alt="instance1" src= "https://github.com/NeyonOndela/AWS-Security/blob/0dd9b3e2b424270be135b947d6c24b1feb1fa590/resources/ec.jpg" />

<img width ="1000" height="500" alt="instance1" src="https://github.com/NeyonOndela/AWS-Security/blob/49072c10d0691dcd9655612c6284a664a1a8a40c/resources/ec6.jpg" />




## Adding Users to Groups
I then added users to specific groups to grant them predefined permissions. Once a user was added to a group, their access level immediately changed based on the group’s attached policies.This demonstrated how IAM simplifies user management. Instead of editing permissions individually for each user, administrators can manage permissions at the group level.

<img width ="1000" height="500" alt="instance1" src="https://github.com/NeyonOndela/AWS-Security/blob/762f3815d6eeec946bca35056babebf97245237d/resources/ec7.jpg" />

## Using the IAM Sign-In URL
The lab also required locating and using the IAM sign-in URL. This URL allows IAM users to log in to the AWS Management Console using their own credentials rather than the root account.Testing login access through the sign-in URL confirmed how policies directly impact what services and actions users can access within the AWS console.


## Testing Policy Effects on Service Access
To fully understand IAM behavior, I experimented with service access using different user accounts. When permissions were restricted, access to certain AWS services was denied. When users belonged to groups with broader permissions, they were able to perform additional actions.
This hands-on testing clarified how:
- Group membership controls access
- Policies define capabilities
- Security is enforced in real time

  <img width ="1000" height="500" alt="instance1" src="https://github.com/NeyonOndela/AWS-Security/blob/e584175a92ed0b81a8bf153be80bf33b86272579/resources/sec2.jpg" />
  <img width ="1000" height="500" alt="instance1" src="https://github.com/NeyonOndela/AWS-Security/blob/c747ae42b53c87ca37728c2796997dddb730cafd/resources/sec3.jpg" />
  <img width ="1000" height="500" alt="instance1" src="https://github.com/NeyonOndela/AWS-Security/blob/a0b540cc38c97ea11170db35e1b0dfe59920fc18/resources/sec4.jpg" />


  
## Key Learning Outcomes
- Through this lab, I gained practical experience in:
- Managing authentication through password policies
- Implementing authorization using IAM groups and policies
- Applying the principle of least privilege
- Understanding policy inheritance
- Securing AWS environments against unauthorized access
I also developed a stronger understanding of how access control in cloud environments differs from traditional on-premises systems.

## Conclusion
This lab provided a foundational understanding of AWS Identity and Access Management and its role in cloud security. IAM is a critical service that ensures secure and controlled access to AWS resources.By creating password policies, managing users and groups, and testing permission boundaries, I developed practical skills in cloud identity management. These skills are essential for designing secure, scalable, and well-governed AWS environments.

**Disclaimer**
This is an academic project created for educational purposes to demonstrate practical understanding of AWS IAM concepts and access control implementation.
