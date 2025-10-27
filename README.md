🚀 SMART AWS COST SAVER – AUTO-CLEANUP OF OLD SNAPSHOTS

Ever wondered why your AWS bill keeps growing even when you’re not using all your servers?
That’s often because of old EBS snapshots — backup copies of your data that just sit there, unused, still costing money.

This project introduces an AWS Lambda-based automation that helps identify and delete such stale snapshots, keeping your AWS environment clean and cost-efficient.

🧩 HOW IT WORKS (IN SIMPLE TERMS)

The Lambda function first retrieves all EBS snapshots from your AWS account.
It then checks all EC2 instances that are currently active (running or stopped).
For each snapshot, it verifies whether the associated volume is linked to any active EC2 instance.
If a snapshot’s volume is not connected to any instance, it is marked as unused and safely deleted.

💡 This automatic cleanup reduces storage costs and ensures efficient resource management.

🛠️ TOOLS & TECHNOLOGIES USED

AWS Lambda – Serverless automation to execute the cleanup logic
Amazon EC2 – Source of snapshot and instance information
Amazon EBS – Stores snapshots that are analyzed and managed
AWS IAM – Provides permissions for Lambda to access EC2 and EBS resources
Python (Boto3 SDK) – Used for scripting and interaction with AWS services
