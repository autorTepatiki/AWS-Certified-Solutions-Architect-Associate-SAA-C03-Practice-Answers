# ⬆️ Amazon Web Services Certified (AWS Certified) Solutions Architect Associate (SAA-C03) Practice Tests Answers
These are my own responses from A.Cantrill's (AWS Certified) Solutions Architect Associate (SAA-C03) Practice Tests #1 & #2 answers.

# Verified Practice exam #1 answers

1 / 64
You are designing infrastructure for a bespoke data analysis application. One of the volumes will host a small temporary data base and require high IOPS. What storage should you suggest?
-	Instance Store

2 / 64
You have a fleet of 10 EC2 instances split across two availability zones, provisioned by an auto-scaling-group and using an application load balancer. The instances ALB is using EC2 status checks and all instances are currently passing 2/2 checks - but some are showing application failures and the instances are not being re-provisioned. What could the problem be? (choose one)
-	ELB Health-Checks are not being used by the ASG


3 / 64
You need to configure 100 EC2 instances for monitoring as part of completing a project. You have been asked to gather metrics on memory utilization. What do you need to do assuming all 100 EC2 instances are t3.large size? (choose one)
- Install the CWAgent


4 / 64
Backup data is being created and placed into S3 in a central location. Objects are being replicated to a bucket in an AWS region closer to some support staff in another part of the world. Your manager has asked you to see if there is a way to reduce the S3 storage costs within this system. What storage classes will you recommend to your manager?
-	Use S3 Standard-Infrequent Access for the central bucket and S3 One Zone-Infrequent Access for the regional bucket

5 / 64
You are helping to implement a web application with about 15,000 users within AWS. The application runs on android and iOS devices and needs an identity provider to use to access AWS products and services. What solution should you suggest? (Choose one)
-	Use an external IDP such as google, and exchange these credentials to access AWS

6 / 64
You have been asked to migrate a large micro service application into AWS which currently uses Docker running on virtual servers. It's been suggested by your client that they can run docker containers on EC2 instances. Which product should you suggest the business uses. They have given you the directive that they care about cost efficacy and low admin overhead equally.
-	ECS Fargate

7 / 64
Which DNS Record type is used to commonly verify domain ownership?
-	TXT


8 / 64
You are encountering performance issues on a EBS GP2 Volume which you suspect are due to the higher than expected IOPS demands. What two tools could you use to confirm your suspicion and fix the issue (choose two)
-	CloudWatch Cloud + EBS IO1

9 / 64
What is true of an eventually consistent read from DynamoDB (Choose all that apply)
-	uses less RCU than a strongly consistent read +  You can receive outdated data

10 / 64
After significant development effort, a User Data script has been developed to bootstrap EC2 instances. The script patches the OS, downloads and installs applications, and configures services. Over time the script has grown, and it now takes around 10 minutes for an instance to complete the launch process. Which method will decrease launch time for the instance while maintaining security and functionality?
-	Create and use a custom AMI that is patched, and has the required applications downloaded and installed. Simplify the bootstrap script to perform instance specific configuration

11 / 64
A mobile app enables users to post and share images on a social media platform. The architecture requires users to upload images through the app to a single S3 bucket in us-east-1. Thousands of images being posted every minute, and users expect real time access to a stream of images from other users around the world. Which solution would you recommend for maximum performance.

-	Enable S3 transfer acceleration

12 / 64
An EC2 instance has been configured with a script in User Data that runs when the instance is booted. The script makes a call to S3 to copy setup and configuration calls. Upon launching the instance you realize that the script is failing as it doesn't have permission to access the S3 bucket containing the resources it needs. What solution will fix the problem while maintaining the best security practices?
-	Associate an IAM role with the EC2 instance that contains permissions to the S3 bucket

13 / 64
You have been asked to implement a configuration allowing access to an S3 bucket in your account to IAM users from an external account. Objects which are uploaded MUST be owned by your account, NOT the external account. Which option meets this requirement ?
-	Use an IAM role in your account
-	(option: bucket-owner: Use a bucket Policy)

14 / 64
Which DNS record type is generally used to point R53 record sets at AWS logical resources
-	A + ALIAS

15 / 64
You are configuring a project with 100,000 IOT devices which are sending telemetry into AWS. You need to perform near real time analytics on the data, which product should you use to ingest the data in a highly available and high performance way? (choose one)
-	Kinesis


16 / 64
You are running a custom application on a small number of EC2 instances and need to configure CloudWatch to log a custom application performance metric. Which two steps would you recommend as part of the solution? The number of instances which run the application might rapidly increase if the application usage grows.
-	Configure IAM roles for the instances + Install the CWAgent and configure it to capture the custom metric

17 / 64
You are reviewing the configuration of a private VPC. The VPC has no internet gateway and instances have no public IPs associated with them. The VPC has a selection of VPC endpoints including S3, DynamoDB, SQS, SSM, SNS and Kinesis. You need to access one of the EC2 instances from the console UI to perform some diagnostics, what is the quickest way of doing so?
-	Use Session Manager

18 / 64
You have an EC2 instance which has been configured badly. You are migrating data off the instance, it uses a volume listed as ephemeral0 which contains critical data which is not replaceable. If you restart this EC2 instance before migrating the data off this volume, will this cause any additional problems ?
-	No, the data will be fine. Only if terminate state happens, data will be lost.

19 / 64
You have been asked to allow an IPv6 EC2 instance to communicate with the public internet, but not allow any access to the instance from the public internet. In addition, IPv4 internet traffic should be allowed in either direction. What VPC products are required to meet this requirement.
-	IGW + Egress-Only Internet Gateway

20 / 64
You are designing a VPC private networking architecture for an application. The application needs to be fully highly available across three availability zones. It has 2 tiers, a web tier and a backend tier, Different security and routing configuration is required for the different tiers. How many subnets (minimum) are required for this solution.
-	6

21 / 64
You need to store files in S3 .. and they need to be encrypted at rest. You need a solution which matches the FIPS 140-2 Level 3 framework the rest of your organisation works within. Which solution meets this requirement? (Choose one)
-	CLOUDHSM + Client-Side Encryption

22 / 64
A scientific processing workload you are wanting to perform is only economical if it can be run at around 40% lower than EC2 on-demand rates. The processing run takes between 3 and 4 days and needs to be run once per month. It can tolerate interruption and just rerun any failed components and is not time critical or predictable. The workload can scale to as many instances as are available. Which pricing model offers the most cost-effective solution for this workload?
-	Spot

23 / 64
Part of an application you manage uses S3 and CloudFront to distribute cat pictures to a global audience. One of your design staff have updated one of the cat images, the original had an image artifact. Users of your application are still seeing the original image. Which of the following could resolve the issue with the least amount of disruption to your customers ?
-	Invalidate the object on the CloudFront Distribution

24 / 64
A client has noticed different storage classes available within S3 and has asked about the Glacier and Glacier deep archive classes - they appear to be cheaper. Which of the following options are ideal use cases for the S3 Glacier Storage class (Choose two)
-	Data Archival + Long Term backup data


25 / 64
AWS provide a registry of open data sets which can be used by customers within their applications. How much does it cost to use these datasets within AWS products?
-	Free

26 / 64
A large enterprise is looking to migrate a large amount of data from local storage to S3 as part of a wider migration. The data is around 500TB and is split across 2 data centers equally and they currently have a 100Mbps internet link from each data centre .. with a 100TB a month bandwidth cap on each link. What is the most efficient and economical way to perform this migration as quickly as possible but at a reasonable cost.

-	Order multiple AWS Snowball devices for each data centre … transfer the data and ship back to AWS for transfer into S3

27 / 64
A administrator working with you on a project is trying to enable S3 Cross-Region replication between two S3 buckets. She is having issues, what could be a potential reason why CRR can’t be enabled?
-	One or both of the buckets might not have versioning enabled

28 / 64
A mission critical EBS volume has 20 GiB of data. A 1st EBS snapshot is taken. 6 GiB of changes are made to the drive before a 2nd snapshot is taken. 2 GiB of further changes are made, before a 3rd snapshot is taken. To save costs the first snapshot is deleted. Which statement best describes what can be recovered from the remaining snapshots?
-	A full recovery can be made to either the state of the 2nd or 3rd snapshot

29 / 64
Which of the following metrics can be obtained by CloudWatch from an EC2 instance WITHOUT needing CWAgent Installed (choose all that apply)
-	Network IN and Out + CPU Usage + Disk Reads and Writes

30 / 64
You have a single EC2 instance running a small public web application. You use an S3 bucket as a ‘maintenance’ page for when the application is offline or has failed. Currently this process is manual, what AWS product and feature can you use to automated this process.
-	Route53 (health-checks policy)

31 / 64
You manage 100's of AWS accounts for your business. One of the accounts is for a development team and you need to restrict what can occur within the account. There are 5 IAM users and the account root user which need to be restricted. What should you suggest? (Choose one)
-	SCP – service control policies

32 / 64
What feature within AWS allows you to control access to an S3 bucket so that everything BUT CloudFront Access is denied ?
-	OAI/OAC : Origin Access Control (OAC) or Origin Access Identity (OAI)

33 / 64
One of your clients is introducing a new system that allows its website users to vote on their favourite celebrity photograph. Their existing website runs well, and is hosted on EC2 m5.8xlarge instances within an auto scaling group. The client expects a large uptake of the new system and is concerned that their existing infrastructure won't cope even though they use CloudFront. What architecture would you recommend for the new system?
-	Develop the new system using Lambda

34 / 64
Which of the following statements are true ?
-	EIP’s are per account, per region + EIPs have a cost if not associated with anything

35 / 64
Your company has a small development team. In order to reduce costs you decide to turn off EC2 instances out of hours and on the weekends. In what state should you place the EC2 instances in order to not lose its configuration.
-	Stopped

36 / 64
Which statement best describes an architecture using an SQS standard queue?
-	System components taking messages from the SQS queue should not require the messages to be in the same order that they were added to the queue, and should be able to handle the same message being delivered twice


37 / 64
You have launched 5 EC2 instances of the same size into a cluster placement group. You attempt to launch 5 more and get an error. What options could explain this, or resolve this ? (choose all that apply)
-	Use the same type and size of instances + Terminate the instances, relaunch 10 into the same placement group


38 / 64
In what scenario would you suggest a Site-to-Site VPN is used rather than a Direct Connect
-	Provisioning Timeframe Priority

39 / 64
You need to configure private networking connectivity between a single on-premises location and AWS. You have been told that low latency and high speeds are a requirement and that the solution needs to be up and running within 4 days. Your on-premises location is in a semi rural location. What solution should you suggest
-	VPN + Direct Connect

40 / 64
You manage the infrastructure for a team of developers, the QA environment is automated and constantly provisions, tests and terminates application environments. The app environment consists of an EC2 instance which is built automatically and contains no valuable data and a MariaDB RDS SingleAZ instance. You have been asked to make sure that before an environment is terminated, backups are taken which last at least 6 months. What should you suggest?
-	Run a manual snapshot of the RDS instance before termination

41 / 64
You are to suggest a solution for a managed SQL database which provides 3+ AZ Automatic Resilience. Which option should you suggest ?
-	 Aurora with replicas in all AZs

42 / 64
A company has a monolithic application that they are refactoring to run in Docker containers. The engineers want to avoid as much infrastructure management as possible so they can focus on the application itself. Which service would you recommend to satisfy these requirements?
-	Fargate

43 / 64
You have modified a CloudFormation template used to create a windows EC2 instance, and changed it to launch a Linux instance. You cannot connect to the instance using SSH. You know the template works for a Windows instance and have just tested and verified that. What could the potential problem be?
-	Make sure TCP/22 is enabled on the instance security group

44 / 64
You have a fleet of EC2 instances, managed by an auto-scaling-group which run a large scale web application. The web servers need to receive a copy of the web root files in a secure way. Which option do you suggest … (choose one)
-	Create an EC2 instance role, pass in commands via cloud-init to download web root from S3

45 / 64
Which of the following AWS products and features can be used to allow network connectivity between two or more VPCs
-	Transit Gateway + VPC Peer

46 / 64
You have a S3 bucket with 100 objects. You have been asked to design a replication solution and choose the built-in Cross Region Replication. You enable the feature, add 50 objects, wait 10 minutes and add a further 75 objects to the bucket. How many objects are in the remote bucket?
-	125 (and NOT 225)

47 / 64
A business has its own data center with file storage for applications within its network. The storage is rapidly reaching capacity and management need a quick solution before it runs out completely. What AWS based architecture would you recommend?
-	Configure AWS Storage Gateway to span the on-premise storage into S3

48 / 64
Which of the following are reasons for using EC2 Enhanced Networking
Additional networking features such as multicast
-	Lower & consistent latency + Better packet per second (PPS) performance

49 / 64
You have been asked to assist with a university enrolment system which uses DynamoDB as a database layer. The system is suffering due to heavy reads in the enrolment period of the university. Load is currently 3-4x the expected amount and 90% of it is read operations checking enrolment status for class sign-ups. What should you suggest to aid in the extra load. The changes should be the least amount of admin overhead possible while being cost effective. The application is serverless, it runs from an S3 bucket and interacts with the DynamoDB endpoints using JS in a browser.
-	Increase RCU ( not DAX ) :  Read-Capacity-Unit : it allows you to perform: 1 strongly consistent read per second for an item up to 4 KB in size, 2 eventually consistent reads per second for an item up to 4 KB in size, 1 transactional read per second for an item up to 4 KB in size, but it requires 2 RCUs.

50 / 64
You have been asked to design a data encryption architecture for medical records. The requirements are that data is sent into AWS in a way where it's encrypted in transit. Your business needs to manage the encryption keys such that they aren't stored in AWS and ideally you don't have the overhead of performing encryption or decryption operations. What is a valid option based on these requirements?
-	SSE-C

51 / 64
You notice that someone has configured CloudFront when they deployed a solution in AWS. Which statement best describes the usual purpose of CloudFront?
-	A content delivery network (CDN)

52 / 64
An application running on EC2 improves its performance by using instance store to persist cache data. Which of the following statements best describes this cache data? CHOOSE THREE ANSWERS
-	The cache data will be lost if the EC2 instance is stopped + The cache data will be lost if the EC2 instance is terminated + The cache data will be lost if the EC2 instance suffers from a hardware failure

53 / 64
Which of the following scenarios is most suitable to be deployed to AWS Lambda? CHOOSE TWO
-	A script that runs every month to trigger maintenance tasks on EC2 instances + A script that processes a text file when that file is uploaded to an S3 bucket

54 / 64
Which statements are true of CloudFront (Choose all that apply)
-	CF can improve performance of static HTTP/S content + CF can improve performance of dynamic HTTP/S content

55 / 64
What is an appropriate and cost-effective use for the S3 storage class Standard-Infrequent Access?
-	Objects stored with 99.999999999% (11 9’s) durability that when requested take milliseconds to be retrieved

56 / 64
You have been asked to implement a solution which can manage an application workflow which runs for between 7 and ~45 minutes before terminating. The process consists of individual steps which run for less than 5 minutes each. The processes are written in Python. Which AWS product or products should you suggest to implement the solution in a cost effective way ? (choose one)
-	Step Functions + Lambda

57 / 64
You are migrating an application into AWS which uses a messaging system to decouple its components (web and worker). Which AWS Service can be used to provide this functionality?
-	SQS

58 / 64
You are migrating a Windows file server into AWS so that it can be used by VPC hosted Workspaces (Virtual Desktops). What is the most cost effective and resilient way to host this data in AWS and provide access to it using the SMB protocol.
-	FSx

59 / 64
Due to compliance requirements, you have been instructed that data within a VPC must NOT traverse the public Internet. The system uses EC2, EBS, EFS and a Direct Connect dedicated network connection from your premises. You have been asked to report on the suitability of the architecture.
-	By default data within this architecture does not traverse the public Internet.

60 / 64
You are noticing that within an auto-scaling-group managing the front-end for a busy application with rapidly changing load levels … instances are being started and terminated rapidly. This is causing disruption to the application and excessive costs. What setting could you change to change this behaviour ?
-	Change the cooldown period

61 / 64
You have recently started a new job. Your manager asks you to review the design of a Site-to-Site VPN Solution to ensure it's highly-available. It uses 1 VGW, 1 VPN connection and 1 CGW. What should you tell your manager? (choose one)
-	Another CGW and VPN Connection is needed for Full HA

62 / 64
You are receiving large SQS bills every month for a queue which is involved in a worker processing tier. The tier has 5 instances which are static and not scaled using an ASG. There appears to be only low volume running through your SQS queue. What would likely reduce bills? (choose 2)
-	Switch to long-polling + Re-provision the instances using an ASG based on queue length

63 / 64
You need configure an EC2 instance so it can only be accessed using SSH from IP 1.3.3.7. Which of the following will implement the desired configuration?
-	Add an SG Inbound 1.3.3.7/32 TCP 22

64 / 64
Your developers are refactoring a legacy application into a series of services. At this stage most of the services are long running processes using chunks of code from the original application. What architecture components would you recommend to make best use of AWS services?
-	Configure the service to Docker containers and deploy with ECS

# Verified Practice exam #2 answers

27 / 61
You have been asked to suggest an AWS product which provides storage which can be mounted on linux instances, supports POSIX type permissions and can be used by multiple instances at the same time. Which option should you suggest?
-	EFS

28 / 61
You have been asked to design encryption for a health care related data set. The requirement is that data be transferred to S3 in an encrypted way. And when on S3 it must be encrypted. S3 Full administrators must not be able to access the data contents, but must be able to manage that data. Analysis staff must be able to access data, but not adjust encryption in any way. The solution should use the least number of services to meet the objectives and have the least admin overhead. What should you suggest ?
-	SSE-KMS (optionally but more complex, SSE-C)

29 / 61
You have recently enhanced an application by using an auto-scaling-group and an application load balancer. Users have reported that the application is constantly logging customers out and losing progress. What is a potential fix for this behaviour ?
-	Enable session stickiness

30 / 61
You are having problems establishing a Dynamic Site-to-Site VPN between AWS and a client site. Which of the following could be a potential reason?
-	The Customer router cannot use BGP

31 / 61
You are launching an application which operates in a controversial area of industry and you are expecting internet based attacks. Your application runs inside a VPC, within an auto-scaling-group and uses an application load balancer. The hostname for the application www.dogsarebetterthancats.com uses an external DNS provider. How can you protect against DDOS attacks with this application?
-	Purchase Shield Advanced

32 / 61
You have 4 VPC’s and need to configure AWS to allow communications between all 4 VPC. Which of the following options will meet that requirement and do so with as little configuration & ongoing admin overhead as possible (choose one)
-	1 Transit Gateway

33 / 61
You are hosting a blog platform in AWS. The blog platform has been developed to use a MySQL 5.7 using the InnoDB storage. To get the best performance from your architecture, what AWS services would you use?
-	EC2 instances and AWS RDS using Aurora

34 / 61
You are the solutions architect in charge of migrating a wordpress hosting business to AWS. They have several clients who consume significant resources. They have asked you to design a multi-instance storage solution for shared data the servers currently use Ubuntu Linux. Which product should you recommend ? (choose one)
-	EFS (just storing, not considering the SQL engine)

35 / 61
You have configured S3 so that when a video file is uploaded, an event is generated. You need two processes to run independently when the video is uploaded, generating two different sizes and then adding a water mark. What service or combination of services would allow this process to take place?
-	SNS + SQS + ASG

36 / 61
You have been alerted to suspect connections being attempted to 100 EC2 instances within an Auto-scaling-group from a group of external IP addresses. There is one range of IP addresses in a /24 network and another single IP address. What is the quickest way to block access to your EC2 instances from these IP addresses.
-	NACL Inbound (and NOT SG inbound)

37 / 61
You are attempting to diagnose a networking problem within a VPC. You have an existing EC2 instance deployed in a subnet with a public IP address. This instance can be accessed from the public internet and it can access anything ON the public internet. You launch an additional EC2 instance in the same VPC subnet and cannot access it from the public internet. What could be a possible reason for this?
-	The instance has no public IP address allocated

38 / 61
After deploying an HPC application across multiple EC2 instances you discover performance issues. Upon investigation you determine that network latency is the cause of the issues. What solution do you suggest to attempt to mitigate the performance issues?
-	Place the EC2 instances in a single Cluster Placement Group

39 / 61
A local police force has asked you to help implement a solution for tracking police units. Every unit has a GPS tracker which transmits data every 60 seconds. You need to suggest a solution which can accept the data en-mass from all units in the country and allow multiple applications to read and process data in near realtime for different business and security functions. What should you suggest?
-	Kinesis

40 / 61
You run an online commerce business which prints images on glass. You would like a long running process (2 weeks) to be initiated whenever an order arrives in a DynamoDB orders table. What AWS products should you use to ensure the most cost-effect solution?
-	DynamoDB Streams, Lambda, Stepfunctions

41 / 61
An animal charity is launching a new campaign and needs a website. The content of the website will explain to users how the campaign works, and provide links to their existing financial partner who deals with charitable donations. This website will be promoted using social media platforms and many thousands of page impressions are expected per minute. What architecture would you recommend to satisfy the charities requirements while keeping costs as low as possible?
-	Create an S3 bucket and enable static web hosting

42 / 61
You have been asked to migrate a system into the cloud in order to reduce the management overheads for your business. The system uses a shared NFS file system for common data used on multiple components of the system. To meet this requirement without major changes to the system what architecture would you recommend?
-	Elastic File System (Amazon EFS)

43 / 61
A Database solution you are implementing requires high throughput and manages high IO workloads. It uses a collection of volumes ranging in size and requires performance which is independent of size. What volume type should you suggest ? (Choose one)
-	IO1 (provisiones IOPS SSD)

44 / 61
You are designing a financial application which requires high IOPS capability on its storage. You have been asked which storage type to suggest. The storage needs to be mountable on an EC2 instances and accessible from one EC2 instance at a time. The data which is being stored is business critical and requires 25,000 IOPS at all times.
-	EBS IO1

45 / 61
You have been asked by the maker of a popular game ‘catcraft’ to implement load balancing for their front end game infrastructure. The game doesn’t use HTTP or HTTPS instead a custom low latency protocol which runs over the top of TCP. The game is expected to be popular and whatever you implement needs to cope with 500,000 requests per second as a starting point and this is expected to scale rapidly. What should you suggested to distribute load over the front end servers
-	NLB (network LB)

46 / 61
Which actions are required to make an EC2 instance publicly accessible on the IPv4 internet.. (Choose all that apply)
-	An attached internet gateway + 0.0.0.0/0 + Public IP4 Address configured on the instance

47 / 61
An application within an architectre you designed 12 months ago is experiencing performance issues. The application runs on a T3.Large instance and uses a MariaDB RDS Multi-AZ database instance. The application is experiencing issues with database writes... and appears constrained. What is the most cost effective way of fixing this problem with no application changes ? (Choose one)
-	Adjust the RDS Instance Size and/or storage type

48 / 61
You are designing an application which uses lambda as the provider of compute. The application is javascript, it loads from an S3 bucket and runs in the browser of customers. It needs to be able to communicate with AWS services such as DynamoDB and as required cause lambda functions to run. Which AWS Service can act as the middleman in this type of architecture? (Choose one)
-	API Gateway

49 / 61
You are reviewing an architecture built in a new AWS account. The architecture centers around a Virtual Private Cloud (VPC). Which of the following statements best describes a VPC?
-	A logically isolated network

50 / 61
You have been asked to create an EC2 instance with network interfaces in two separate subnets. What should your response be?
-	Possible only if subnets are in the same AZ

51 / 61
A news organization uploads articles to S3 for internal use. Articles uploaded in the last month will be accessed by staff regularly, with articles older than 3 months are unlikely to be used again but should be archived. Which of the following solutions will keep storage costs as low as possible while meeting requirements?
-	Configure an S3 lifecycle policy that will transition objects to the S3 Glacier storage class after 90 days

52 / 61
A client is launching a cat image sharing website called catagram. It needs a high performance, scalable, resilient and publically accessible location to store images of various sizes. The application needs to be able to provide time limited access to the objects to protect the rights of content owners. Which product should you select.
-	S3

53 / 61
You have an on-premises active directory and have connected this network to an AWS VPC using a site-to-site VPN connection. You intend to perform a Workspaces Proof of Concept pilot. What do you need to do before deploying workspaces (choose one).
-	Use AD Connector

54 / 61
A legacy linux application is running on 5 virtual servers on-premises and needs to be migrated to AWS. It uses multicast networking and this can’t be changed. How can this be migrated into AWS, are any special accomodations needed ?
-	Build the servers within an ASG/LT, create an multicast network overlay internally within the OS networking.

55 / 61
Your business is merging with another company over the coming 12 months. Long term the plan is to create a new AWS account infrastructure and move into this for the new shared entity. Your business has 3000 staff, the other business has 2500. You have been asked to give the 2500 staff access to your AWS account as quickly as possible, while keeping the admin overhead low. What should you suggest?
-	Use an IAM role

56 / 61
Assuming you have allocated a keypair when launching a public EC2 instance and have network connectivity .. which of the following ways are valid for logging into a linux EC2 instance
-	Local SSH client using key authentication + EC2 Instance Connect

57 / 61
An application uses a worker pool architecture consisting of an auto-scaling-group which scales based on the length of an SQS Queue. Permissions to access the queue for work, and to write the output to S3 is provided via an instance role assigned at launch to the EC2 instances. Recently the length of the queue has started to increase as has EC2 costs. Jobs are getting processed, but you are experiencing additional errors. What could be the problem?
-	No dead letter queue (to avoid invalid messages to be processed for ever)

58 / 61
A VPC you manage has a collection of 10 EC2 instances running across two AZs in two private subnets, with IPv4 addresses only. You need to make sure the instances have outgoing only access to the internet. What should you do?
-	Deploy a NATGateway

59 / 61
You have added a rule to a NACL which allows traffic through to a VPC subnet but are finding that its not working as expected. What possible things should you investigate? (Choose all which apply)
-	NACL rules are stateless make sure you have a rule for the response traffic
-	NACL rules are processed in order, make sure there isn’t one with a lower number which is processed first
-	Make sure the NACL is assigned to the correct subnet

60 / 61

A member of your clients IT team has suggested that enabling Multi-AZ on a MySQL RDS instance will help improve performance. You have been asked to comment, what should you say?
-	Multi-AZ only helps with availability










































