- [Amazon EBS](#amazon-ebs)
- [Cloudwatch](#cloudwatch)
- [AWS Identity and Access Management](#aws-identity-and-access-management)
- [RDS](#rds)

## Amazon EBS
---

- <b> Amazon EBS </b> provides three volume types to best meet the needs of your workloads: 
    - <b> General Purpose (SSD) </b>
        - General Purpose (SSD) volumes are suitable for a <u>broad range of workloads, including small to medium-sized databases, development and test environments, and boot volumes.</u>
    - <b> Provisioned IOPS (SSD) </b>
        - These volumes offer storage with consistent and low-latency performance and are designed for I/O intensive applications such as <u>large relational or NoSQL databases. </u>
    - <b>Magnetic</b>
        - for workloads where <u>data are accessed infrequently, and applications where the <i>lowest storage cost</i> is important. </u>

## Cloudwatch
---
- Monitoring tool for your AWS resources and applications.
- <u> Display metrics and create alarms </u> that watch the metrics and send notifications or automatically make changes to the resources you are monitoring when a threshold is breached.

## AWS Identity and Access Management
---
- You can use an <i><u>IAM role to specify permissions for users </u></i> whose identity is federated from your organization or a third-party identity provider (IdP).
    - <b>Federating users with SAML 2.0</b>
        - If your organization already uses an identity provider <u>software package that supports SAML 2.0 (Security Assertion Markup Language 2.0)</u>, you can create trust between your organization as an identity provider (IdP) and AWS as the service provider. 
        - You can then use SAML to provide your users with <u>federated single-sign on (SSO) </u>to the AWS Management Console or federated access to call AWS API operations. 
        - <b>For example</b>: if your company uses Microsoft Active Directory and Active Directory Federation Services, then you can federate using SAML 2.0
    - <b>Federating users by creating a custom identity <u>broker application</u></b>
        - If your <u>identity store is not compatible with SAML 2.0,</u> then you can <i>build a custom <b>identity broker application </b> to perform a similar function. </i>
        - The broker application <u>authenticates users, requests temporary credentials for users from AWS,</u> and then provides them to the user to access AWS resources.
        - The application verifies that employees are signed into the existing corporate network's identity and authentication system, which might use LDAP, Active Directory, or another system. The identity broker application then obtains temporary security credentials for the employees.
        - To <i>get temporary security credentials, </i>the identity broker application calls either `AssumeRole` or `GetFederationToken` to obtain temporary security credentials, depending on how you want to manage the policies for users and when the temporary credentials should expire.
        - The <u>call returns temporary security credentials consisting of an AWS access key ID, a secret access key, and a session token.</u> The identity broker application makes these temporary security credentials available to the internal company application. 

            <img src="./images/Overview/broker-application.jpg" width="47%" height="40%"/>
        - This scenario has the following attributes:

            - The identity broker application has permissions to access IAM's token service (STS) API to create temporary security credentials.

            - The identity broker application is able to verify that employees are authenticated within the existing authentication system.

            - Users are able to get a temporary URL that gives them access to the AWS Management Console (which is referred to as single sign-on).
