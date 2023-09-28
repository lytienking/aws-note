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
172: With Amazon CloudFront, you can enforce secure end-to-end connections to origin servers by using HTTPS. Field-level encryption adds an additional layer of security that lets you protect specific data throughout system processing so that only certain applications can see it.
174: auto scaling groups can not span multi region
178: Using AWS Backup is a simple and efficient way to backup EC2 instances and RDS databases to a separate region
179:
180: AWS WAF deploy on Application Load Balancer, API Gateway, CloudFront, AppSync GraphQL API, Cognito User Pool
181:
184:
185: To ensure that an Amazon Elastic Container Service (ECS) application has permission to access Amazon Simple Storage Service (S3), the correct solution is to create an AWS Identity and Access Management (IAM) role with the necessary S3 permissions and specify that role as the taskRoleArn in the task definition for the ECS application
186: EFS is not compatible with Windows
194:
200: use an Amazon Cognito user pool authorizer in API Gateway. This will allow Amazon Cognito to validate each request and ensure that only authenticated users can access the API
201: With Amazon Pinpoint, you can create automatic responses when customers send you messages that contain certain keywords.
204: manage fine-grained permissions -> lake formation
206: Event bridge was built specifically to handle this kind of scenario:
CreateImage API call (Event Source) -> Event bus -> Rules - > Amazon SNS (Event target)
215: 500 Mbps of dedicated bandwidth -> snowball
218: The default network ACL has been modified to block all traffic -> 32768-65535 to destination 0.0.0.0/0 
219: "in-memory tasks" => need the "R" EC2 instance type to archive memory optimization. So we are concerned about C & D. Because EC2 instances don't have built-in memory metrics to CW by default. As a result, we have to install the CW agent to archive the purpose
222: the vendor -> iam role
225:
226: RESTful web services
227: 4 năm -> Configure the S3 Lifecycle policy to delete previous versions as well as current versions.
235: Because we need SCT to convert from Oracle to PostgreSQL, and we need memory optimized machine for databases not compute optimized
237:
240: 
243: file-based applications -> file gateway
246: internet-facing -> tạo public subnets
247: recommends adding a read replica. -> by setting the backup retention period to a value other than 0.
250: There's a table here that specifies that VPC Flow logs can go directly to S3.
253:
254: principle of least privilege -> chỉ allow SG của nhau
260: Active Directory to restrict access.
261: NLB only support Protocol & Port (Not host/based routing like ALB). Lambda@Edge customize CDN
264: 10 EC2 -> ALB performs health checks on the EC2 instances, so it will only route traffic to healthy instances. This avoids the timeout errors
265: MOST secure -> ALB public subnet + EC2 private subnet
266:
273: Backup and Restore -> pilot Light -> warm standby -> Multi Site
274:
276: 
277:
278: Data in hierarchies : Amazon DynamoDB
279: AWS backup hỗ trợ tất cả loại DB , EC2, EBS, EFS, FSx, Volumn gateway back up thường xuyên (giờ ngày tháng) có thể chuyển vô Cold Storage và có cả retention period, Supports cross-region backups, Supports cross-account backups
283: Amazon FSx for NetApp ONTAP storage linux window
287:
291: does not support cookies + change the hardcoded URLs -> Signed cookies + Signed URLs
292: Amazon Managed Streaming for Apache Kafka (Amazon MSK) to stream the data
299: Keyword here is a minimum throughput of 6 GBps. Only the FSx for Lustre with SSD option gives the sub-milli response and throughput of 6 GBps or more
300: thuê hết luôn cho rẻ
302: Use Amazon Elastic Transcoder to convert the video files to more appropriate formats.
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
396: AWS Shield Advanced provides additional protections against more sophisticated and larger attacks for your applications running on Amazon Elastic Compute Cloud (EC2),Network Load Balancing(NLB), Elastic Load Balancing (ELB), Amazon CloudFront, AWS Global Accelerator, and Route 53.
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
423: identity-based policy used for role and group
425: In this case, since the company's daily peak input and output transactions per second are not more than 15,000 IOPS, GP3 volumes provide a suitable and cost-effective option for their workloads.
428:
429:
430:
431:
433: AWS Organizations -> SCP
434: DNS failover
435:
436: "without adding infrastructure" means scaling vertically and choosing larger instance.
437: AWS WAF (Web Application Firewall) is a service that provides protection for web applications against common web exploits. By associating AWS WAF with the Application Load Balancer (ALB), you can inspect incoming traffic and define rules to allow or block requests based on various criteria.
440:
442: you can define tags and tag-based policies to grant selective access to the required data for the engineering team accounts
443:
444: It is the only one with High Availability. Amazon RDS with Multi AZ EC2 with Auto Scaling Group in Multi Az
451:
452: AWS Lambda automatically scales resources to handle the workload, so you don't have to worry about managing the underlying infrastructure
454: AWS Workload Discovery - create diagram, map and visualise AWS resources across AWS accounts and Regions
455: 
459: User-defined cost allocation tags
460: Amazon AppFlow is a fully managed integration service that allows you to securely transfer data between different SaaS applications and AWS services. It provides built-in encryption options and supports encryption in transit using SSL/TLS protocols. With AppFlow, you can configure the data transfer flow from Salesforce to Amazon S3, ensuring data encryption at rest by utilizing AWS KMS CMKs.
465:
468: Private VPC Link: To enable the REST API in API Gateway to access the backend services hosted in Amazon ECS, you can create a private VPC link
470: EIGW for IPv6
474: AWS Transit Gateway is a network hub that you can use to connect your VPCs and on-premises networks. It provides a single point of control for managing your network traffic, and it can help you to reduce the number of connections that you need to manage. Transit Gateway peering allows you to connect two Transit Gateways in different Regions. This can help you to create a global network that spans multiple Regions.
476: 
477:
479: Just Think Infrastructure as Code=== Cloud Formation
481: đúng nhưng note: In the write-through caching strategy, when a customer adds or updates an item in the database, the application first writes the data to the database and then updates the cache with the same data. This ensures that the cache is always synchronized with the database, as every write operation triggers an update to the cache.
483: Using Amazon ECS scheduled tasks on Fargate eliminates the need to provision EC2 resources. You pay only for the duration the task runs. Scheduled tasks handle scheduling the jobs and scaling resources automatically. This is lower cost than managing your own scaling via Lambda or Batch.
484: 
485: Expedited 1->5 mins
490: Export the data directly from DynamoDB to Amazon S3 with continuous backups
491: Add the kms:Decrypt permission for the Lambda execution role
493: 
495: Amazon Macie is a fully managed data security and data privacy service that uses machine learning and pattern matching to discover and protect your sensitive data in AWS. Macie helps identify and alert you to sensitive data, such as personally identifiable information (PII)
498: S3 Lifecycle policies allow you to define rules that automatically transition or expire objects based on their age or other criteria
499: company need to setup a cheaper connection (200 M) but B is incorrect because you can only order port speeds of 1, 10, or 100 Gbps for more flexibility you can go with hosted connection, You can order port speeds between 50 Mbps and 10 Gbps.
500:
502: Managed NFS (network file system) that can be mounted on many EC2
503: monitor data in customer AWS accounts -> IAM role
506: 
507: Amazon DynamoDB global tables is a fully managed, serverless, multi-Region, and multi-active database. Global tables provide you 99.999% availability, increased application resiliency, and improved business continuity. As global tables replicate your Amazon DynamoDB tables automatically across your choice of AWS Regions, you can achieve fast, local read and write performance.