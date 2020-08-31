# AWS 

AWS stands for Amazon Web Service; 
it is a collection of remote computing services also known as a cloud computing platform. This new realm of cloud computing is also known as IaaS or Infrastructure as a Service.
 
## key components of AWS  
- Route 53: A DNS web service
- Simple E-mail Service: It allows sending e-mail using RESTFUL API call or via regular SMTP
- Identity and Access Management:
It provides enhanced security and identity management for your AWS account. AMI stands for Amazon Machine Image. 
It’s a template that provides the information (an operating system, an application server, and applications) required to launch an instance, which is a copy of the AMI running as a virtual server in the cloud.  You can launch instances from as many different AMIs as you need. From a single AMI, you can launch multiple types of instances.  An instance type defines the hardware of the host computer used for your instance. Each instance type provides different computer and memory capabilities.  Once you launch an instance, it looks like a traditional host, and we can interact with it as we would with any computer.
AMI includes: A template for the root volume for the instance, Launch permissions decide which AWS accounts can avail the AMI to launch instances, A block device mapping that determines the volumes to attach to the instance when it is launched
- Simple Storage Device or (S3): It is a storage device and the most widely used AWS service.S3 stands for Simple Storage Service. You can use S3 interface to store and retrieve any amount of data, at any time and from anywhere on the web.  For S3, the payment model is “pay as you go.”
The default storage class is a Standard frequently accessed.
- Elastic Compute Cloud (EC2): It provides on-demand computing resources for hosting applications. It is handy in case of unpredictable workloads
- Elastic Block Store (EBS): It offers persistent storage volumes that attach to EC2 to allow you to persist data past the lifespan of a single Amazon EC2 instance
- CloudWatch: To monitor AWS resources, It allows administrators to view and collect key Also, one can set a notification alarm in case of trouble.


types of AMI provided by AWS are:Instance store backed, EBS backed
The boot time for an Amazon instance store-backend AMI is less than 5 minutes.
We can’t be able to connect EBS volume to multiple instances.  Although, you can connect various EBS Volumes to a single instance.


##  Amazon S3, EC2

Amazon S3 is a REST service, and you can send a request by using the REST API or the AWS SDK wrapper libraries that wrap the underlying Amazon S3 REST API.
By default, you can create up to 100 buckets in each of your AWS accounts.
difference between EC2 and Amazon S3 is that
|EC2|	S3|
| --- | --- |
|It is a cloud web service used for hosting your application |  It is a data storage system where any amount of data can be stored|
|It is like a huge computer machine which can run either Linux or Windows and can handle application like PHP, Python, Apache or any databases |  It has a REST interface and uses secure HMAC-SHA1 authentication keys|
EC2 officially launched in the year 2006.
The buffer is used to make the system more robust to manage traffic or load by synchronizing different component.  Usually, components receive and process the requests in an unbalanced way. With the help of buffer, the components will be balanced and will work at the same speed to provide faster services.
Currently Amazon VPI not provide support for broadcast or multicast.
VPC stands for Virtual Private Cloud. It allows you to customize your networking configuration. It is a network which is logically isolated from another network in the cloud. It allows you to have your IP address range,  internet gateways, subnet and security groups
5 VPC Elastic IP addresses are allowed for each AWS account.  It’s only possible between VPCs in the same region.
A large section of IP Address divided into chunks is known as subnets. You can have 200 subnets per VPC.
Internet gateway is needed to use VPC (virtual private cloud peering) connections.

Edge location is the area where the contents will be cached. So, when a user is trying to accessing any content, the content will automatically be searched in the edge location.
Snowball is a data transport option. It used source appliances to a large amount of data into and out of AWS. With the help of snowball, you can transfer a massive amount of data from one place to another. It helps you to reduce networking costs.

## Instances
vertically scale an Amazon instance 
- Spin up a new larger instance than the one you are currently running
-  Pause that instance and detach the root webs volume from the server and discard
-  Then stop your live instance and detach its root volume
-  Note the unique device ID and attach that root volume to your new server
-  And start it again
 
T2 instances are designed to provide moderate baseline performance and the capability to burst to higher performance as required by the workload.

Types of instances:
-  General purpose
-  Computer Optimized
-  Memory Optimized
-  Storage Optimized
-  Accelerated Computing
 
SimpleDB is a data repository of structure record which encourages data doubts and indexing both S3 and EC2are called SimpleDB.

Amazon Elasticcache is a web service which makes it easy to deploy, scale and store data in the cloud.

Lambda is an Amazon compute service which allows you to run code in the  AWS Cloud without managing servers.

AWS Edge locations are service which redundantly cache data and images.

A Geo-restriction feature helps you to prevent users of specific geographic locations from accessing content which you’re distributing through a CloudFront web distribution.

EMR is a survived cluster stage which helps you to interpret the working of data structures before the intimation.  Apache Hadoop and Apache Spark on the Amazon Web Services helps you to investigate a large amount of data. You can prepare data for the analytics goals and marketing intellect workloads using Apache Hive and using other relevant open source designs.

## Security 

VPC with private and public subnets, database servers should ideally be launched in subnet:
With private and public subnets in VPC, database servers should ideally launch into private subnets.
  security best practices for Amazon EC2 are?
For secure Amazon EC2 best practices, follow the following steps
- Use AWS identity and access management to control access to your AWS resources
- Restrict access by allowing only trusted hosts or networks to access ports on your instance
- Review the rules in your security groups regularly
- Only open up permissions that you require
- Disable password-based login, for example, launched from your AMI

Key-pairs are secure login information for your virtual machines. To connect to the instances, you can use key-pairs which contain a public-key and private-key.

Roles are used to providing permissions to entities which you can trust within your AWS account. Roles are very similar to users. However,  with roles, you do not require to create any username and password to work with the resources

## Cloud services
 
Various types of cloud services are:
- Software as a Service (SaaS),
- Data as a Service (DaaS)
- Platform as a Service (PaaS)
- Infrastructure as a Service (IaaS).


Different layers of cloud architecture are:
- Cloud controller
- Cluster controller
- Storage Controller
- Node Controller

Storage classes available with Amazon s3 are:
- Amazon S3 standard
- Amazon S3 standard-infrequent Access
- Amazon S3 Reduced Redundancy Storage
- Amazon Glacier

DB engines which can be used in AWS RDS
- MS-SQL DB
- MariaDB
- MYSQL DB
- OracleDB
- PostgreDB

should select provisioned IOPS storage over standard RDS storage if you want to perform batch-related workloads.
