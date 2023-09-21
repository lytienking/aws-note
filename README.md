# aws-note
51:
56:
60: a listener rule on the ALB that redirects HTTP traffic to HTTPS
62: đúng như note external certificate authority (CA) => manually 
68: sài Direct connection and Site to site VPN backup connection
70: NLB không hỗ trợ HTTP/HTTPS health check
71: The best solution to meet the RPO and RTO requirements would be to use DynamoDB point-in-time recovery (PITR)
80: Modify the launchPermission property of the AMI. Share the AMI with the MSP Partner's AWS account only. Modify the key policy to allow the MSP Partner's AWS account to use the key.
81: decoupled = SQS, Launch template = AMI, Launch configuration = EC2
94: SQS + lambda + Json to DynamoDB


133: underlying => RDS Custom
137: Use a group email address for the management account's root user
139: S3 không thể gửi notify đến SagaMaker
140: EC2 instance Savings Plans are not applied to Fargate or Lambda
150: Composite Alarm 
306: cluster high network throughput
308: Use the Trusted Advisor recommendations from the consolidated billing account + Review the Trusted Advisor check for Amazon RDS Idle DB Instances.
309: S3 Storage Lens is a fully managed S3 storage analytics solution that provides a comprehensive view of object storage usage, activity trends, and recommendations to optimize costs
314: Aurora Serverless for MySQL => without selecting a particular instance type
315: Amazon Inspector Reporting & integration with AWS Security Hub
316: By migrating the script to AWS Lambda, the company can take advantage of the auto-scaling feature of the service. AWS Lambda will automatically scale resources to match the size of the workload.
377: Amazon EC2 Auto Scaling lifecycle hooks
382: Network Load Balancers now support TLS protocol. With this launch, you can now offload resource intensive decryption/encryption from your application servers to a high throughput, and low latency Network Load Balancer
387: 
388: Security group defaults block all inbound traffic..Add an inbound rule to the security group of the database tier’s RDS instance to allow traffic from the web tiers security group
