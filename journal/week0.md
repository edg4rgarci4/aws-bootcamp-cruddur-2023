# Week 0 — Billing and Architecture

## Required Homework

### Watched Week 0 - Live Streamed Video

- Attended session live

### Watched Chirag's Week 0 - Spend Considerations
- Watched recorded video

### Watched Ashish's Week 0 - Security Considerations
- Watched recorded video

### Recreate Conceptual Diagram in Lucid Charts or on a Napkin
- ![Conceptual Diagram](https://github.com/edg4rgarci4/aws-bootcamp-cruddur-2023/blob/f490d8ea98dd6f9e79802c31e3feab0a190adf1e/journal/assets/Week%200%20Cruddur%20-%20Conceptual%20Diagram.png?raw=true)
- [Lucidchart link](https://lucid.app/lucidchart/afe811be-5a1d-4ce3-a271-ba87b2a122e3/edit?viewport_loc=-3761%2C-307%2C2035%2C1133%2C0_0&invitationId=inv_31bd2875-5e15-41fc-8707-0368076fab6b).
### Recreate Logical Architecture Diagram in Lucid Charts
- ![Logical Diagram](https://github.com/edg4rgarci4/aws-bootcamp-cruddur-2023/blob/f490d8ea98dd6f9e79802c31e3feab0a190adf1e/journal/assets/Week%200%20Cruddur%20-%20Architecture%20Diagram.png?raw=true)
- [Lucidchart link](https://lucid.app/lucidchart/8318855e-efe6-464a-bfdd-386492086284/edit?viewport_loc=22%2C-271%2C3484%2C1939%2C0_0&invitationId=inv_c76749b4-c7f0-44e4-ad54-6c41714aaa2c).
### Create an Admin User
- Created IAM user with Admin privliged attached. Created a new group that this user is a member of and attached the required Admin permission policies to the group. 

### Use CloudShell
![CloudShell](https://github.com/edg4rgarci4/aws-bootcamp-cruddur-2023/blob/f490d8ea98dd6f9e79802c31e3feab0a190adf1e/journal/assets/Week%200%20CloudShell.png?raw=true)

### Installed AWS CLI
- Install via the Gitpod configuration files. Commit [here](https://github.com/edg4rgarci4/aws-bootcamp-cruddur-2023/commit/17eee9668e2619a3affe6d89bb5d4cf0d035bedf). 

### Create a Billing Alarm
- Did this manually and via the CLI. Commit [here](https://github.com/edg4rgarci4/aws-bootcamp-cruddur-2023/commit/77ce6c9ac057626d99daab9b06d7e575286e16cf).
![Billing and Budget Alarm](https://github.com/edg4rgarci4/aws-bootcamp-cruddur-2023/blob/f490d8ea98dd6f9e79802c31e3feab0a190adf1e/journal/assets/Week%200%20Billing%20and%20Budget%20Alarm.png?raw=true)

### Create a Budget
- Did this manually and via the CLI. Commit [here](https://github.com/edg4rgarci4/aws-bootcamp-cruddur-2023/commit/77ce6c9ac057626d99daab9b06d7e575286e16cf).


## Homework Challenges

### Suggested:
- Destroy your root account credentials, Set MFA, IAM role
  - I didn’t “destroy” the root account credentials but I enabled a hardware MFA key for it and stashed that away safely. I created an IAM User with administrative rights to use. 
- Use EventBridge to hookup Health Dashboard to SNS and send notification when there is a service health issue.
  - I did this with awscli commands in GitPod. More proof of credentials  🙂 
  - ![EventBridge AWS Health Alert](https://github.com/edg4rgarci4/aws-bootcamp-cruddur-2023/blob/main/journal/assets/Week%200%20Homework%20Challenge%20EventBridge%20Health%20Alerts.png?raw=true)
### Own:
- Added some security detail to the architecture and conceptual diagrams. I was curious about how this may be documented as I don’t have much experience with diagrams. This led me to this documentation from AWS <https://d1.awsstatic.com/whitepapers/Security/DDoS_White_Paper.pdf> that I took more time to read on. 

- I thought it would be fitting to read up on “[Changes to AWS Billing, Cost Management, and Account Consoles Permissions](https://aws.amazon.com/blogs/aws-cloud-financial-management/changes-to-aws-billing-cost-management-and-account-consoles-permissions/)” as I noticed that banner and its relevant to week 0’s topic. I Had created a “BudgetFullAccess” policy that I modified with the JSON below after reading the AWS blog post: 
```
{
    "Version": "2012-10-17",
    "Statement": [
        {
            "Sid": "ThesePermissionsWillHaveNoEffectTillEndOfMigration",
            "Effect": "Allow",
            "Action": [
                "ce:Get*",
                "ce:Describe*",
                "ce:List*",
                "account:GetAccountInformation",
                "billing:Get*",
                "payments:List*",
                "payments:Get*",
                "tax:List*",
                "tax:Get*",
                "consolidatedbilling:Get*",
                "consolidatedbilling:List*",
                "invoicing:List*",
                "invoicing:Get*",
                "cur:Get*",
                "cur:Validate*",
                "freetier:Get*"
            ],
            "Resource": "*"
        },
        {
            "Sid": "ThisPermissionWillContinueProvidingAccessAsNormal",
            "Effect": "Allow",
            "Action": [
                "aws-portal:ViewBilling",
                "aws-portal:ModifyBilling",
                "budgets:ViewBudget",
                "budgets:ModifyBudget"
            ],
            "Resource": "*"
        },
        {
            "Action": [
                "cloudwatch:*"
            ],
            "Resource": "*",
            "Effect": "Allow"
        },
        {
            "Action": [
                "sns:*"
            ],
            "Resource": "*",
            "Effect": "Allow"
        }
    ]
}
```
