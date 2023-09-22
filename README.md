# aws-note

2: Athena Amazon Athena is an interactive query service that makes it easy to analyze data directly in Amazon Simple Storage Service (Amazon S3) using standard SQL.
3: aws:PrincipalOrgID Validates if the principal accessing the resource belongs to an account in your organization. https://aws.amazon.com/blogs/security/control-access-to-aws-resources-by-using-the-aws-organization-of-iam-principals/
4: VPC xem lại nha mài
5: Concurrent or at the same time key word for EFS
12:
13: With Secrets Manager, you can store, retrieve, manage, and rotate your secrets, including database credentials, API keys, and other secrets
16: Amazon QuickSight only support users(standard version) and groups (enterprise version)
17: Always remember that you should associate IAM roles to EC2 instances
26: AWS Config is a service that enables you to assess, audit, and evaluate the configurations of your AWS resources.
29: AWS Global Accelerator automated failover
41: Keywords: SaaS --> AppFlow Operational overhead (B) vs configuration overhead (A)
49:
50: AWS Systems Manager Run Command allows the company to run commands or scripts on multiple EC2 instances
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
107:
116: We can configure CloudFront to require HTTPS from clients (enhanced security) storing static website on S3 provides scalability and less operational overhead
117: you can stream logs from CloudWatch Logs directly to OpenSearch
120:
121: You can enable encryption for an Amazon RDS DB instance when you create it, but not after it's created. However, you can add encryption to an unencrypted DB instance by creating a snapshot of your DB instance, and then creating an encrypted copy of that snapshot. You can then restore a DB instance from the encrypted snapshot to get an encrypted copy of your original DB instance
122:
127: Max instance store possible at this time is 30TB for NVMe which has the higher I/O compared to EB
133: underlying => RDS Custom
137: Use a group email address for the management account's root user
139: S3 không thể gửi notify đến SagaMaker
140: EC2 instance Savings Plans are not applied to Fargate or Lambda
150: Composite Alarm
151: AWS Control Tower + AWS Organizations
152:
156: Lake information to identify data
157:
168: Service control policies (SCPs) are one type of policy that you can use to manage your organization
170: WAF also Size constraints, geo-match (block countries)
181:
184:
185: To ensure that an Amazon Elastic Container Service (ECS) application has permission to access Amazon Simple Storage Service (S3), the correct solution is to create an AWS Identity and Access Management (IAM) role with the necessary S3 permissions and specify that role as the taskRoleArn in the task definition for the ECS application
186: EFS is not compatible with Windows
194:
200: use an Amazon Cognito user pool authorizer in API Gateway. This will allow Amazon Cognito to validate each request and ensure that only authenticated users can access the API

306: cluster high network throughput
308: Use the Trusted Advisor recommendations from the consolidated billing account + Review the Trusted Advisor check for Amazon RDS Idle DB Instances.
309: S3 Storage Lens is a fully managed S3 storage analytics solution that provides a comprehensive view of object storage usage, activity trends, and recommendations to optimize costs
310:
314: Aurora Serverless for MySQL => without selecting a particular instance type
315: Amazon Inspector Reporting & integration with AWS Security Hub
316: By migrating the script to AWS Lambda, the company can take advantage of the auto-scaling feature of the service. AWS Lambda will automatically scale resources to match the size of the workload.
325:
327: Network Firewall protect your VPC
330: Key Management Service. Secrets Manager is for database connection strings.
335: "EBS fast snapshot restore": minimizes initialization latency
338: Aurora global database 1 Primary Region (read / write), Up to 5 secondary (read-only) regions, replication lag is less than 1 second, Up to 16 Read Replicas per secondary region
344: Amazon SQS has a limit of 256 KB for the size of messages. To handle messages larger than 256 KB, the Amazon SQS Extended Client Library for Java can be used.
351: Step Functions is based on state machines and tasks. A state machine is a workflow. A task is a state in a workflow that represents a single unit of work that another AWS service performs. Each step in a workflow is a state
352: AWS Global Accelerator = TCP/UDP minimize latency
353: RDS does not support IO2 or IO2express . GP2 can do the required IOPS RDS supported Storage > https://docs.aws.amazon.com/AmazonRDS/latest/UserGuide/CHAP_Storage.html GP2 max IOPS >
360:
361:
362:
362:
364:
366:
368: overall password policy
369:
377: Amazon EC2 Auto Scaling lifecycle hooks
382: Network Load Balancers now support TLS protocol. With this launch, you can now offload resource intensive decryption/encryption from your application servers to a high throughput, and low latency Network Load Balancer
387:
388: Security group defaults block all inbound traffic..Add an inbound rule to the security group of the database tier’s RDS instance to allow traffic from the web tiers security group
395: Amazon Inspector evaluate only for EC2 instances, Container Images & Lambda functions
396: AWS Shield Advanced provides additional protections against more sophisticated and larger attacks for your applications running on Amazon Elastic Compute Cloud (EC2), Elastic Load Balancing (ELB), Amazon CloudFront, AWS Global Accelerator, and Route 53.
399: AWS WAF HTTP headers, HTTP body, or URI strings Protects from common attack - SQL injection and Cross-Site Scripting (XSS)

402:
403: To grant the necessary permissions to an AWS Lambda function to upload files to Amazon S3, a solutions architect should create an IAM execution role with the required permissions and attach the IAM role to the Lambda function
405:
410: Create the EBS volumes as encrypted volumes. Attach the EBS volumes to the EC2 instances
413: Amazon SES is a simple and effective solution that can reduce the time spent resolving complex email delivery issues and minimize operational overhead.
416:
417:
418:
419:
422:
