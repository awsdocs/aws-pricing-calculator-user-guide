# Generating Windows Server and SQL Server on Amazon EC2 estimates<a name="windows-workload-estimates"></a>

You can use the workload calculator in AWS Pricing Calculator to guide you on AWS tenancy qualifications for Microsoft Windows Server and SQL Server on Amazon Elastic Compute Cloud \(Amazon EC2\)\. You can use the workload calculator to estimate AWS cost using minimal information and parameters\. You can generate an estimate even if you don't know the details for each parameter\. This is because each parameter includes a default setting\.

For options for using Microsoft software licenses on the AWS Cloud, see [Microsoft Licensing on AWS](http://aws.amazon.com/windows/resources/licensing/)\.

**To generate an estimate for Windows Server and SQL Server on Amazon EC2**

1. Open AWS Pricing Calculator at [https://calculator\.aws/\#/](https://calculator.aws/#/)\.

1. Choose **Create estimate**\.

1. Under **Windows Server and SQL Server on Amazon EC2**, choose **Configure**\.

1. On the **Configure Windows Server and SQL Server on Amazon EC2** page, choose your customized settings\.
   + For information about your tenancy choices, see [Licensing and tenancy recommendations](#estimate-workload-tenancy)\.
   + For information about how to choose your machine specifications, see [Configuring machine specifications](#estimate-workload-configure)\.
   + For information about how to choose your pricing strategy, see [Pricing strategy](#estimate-workload-pricing)\.
   + For information about how to choose your cost details, see [Cost details](#estimate-workload-cost)\.

1. Choose **Add to my estimate**\.

For a step\-by step example shows how to generate an estimate for Windows Server and SQL Server on Amazon EC2, see [Tutorial: Using Windows Server and SQL Server on Amazon EC2 calculator](estimate-workload-tutorial.md)\.

**Topics**
+ [Tutorial: Using Windows Server and SQL Server on Amazon EC2 calculator](estimate-workload-tutorial.md)
+ [Licensing and tenancy recommendations](#estimate-workload-tenancy)
+ [Configuring machine specifications](#estimate-workload-configure)
+ [Pricing strategy](#estimate-workload-pricing)
+ [Cost details](#estimate-workload-cost)

## Licensing and tenancy recommendations<a name="estimate-workload-tenancy"></a>

You can determine your AWS licensing and tenancy options for your workload through your choices for Windows Server and SQL Server licensing inputs\. The licensing options include AWS provided licenses with License Included \(LI\) offerings, and your existing licenses with Bring Your Own License \(BYOL\) offerings for optimal cost savings\. You can identify the most suitable cloud tenancy, for example, Shared tenancy or Dedicated Hosts\.


**AWS licensing and tenancy scenarios supported by AWS Pricing Calculator**  

| Windows Server | SQL Server | AWS tenancy | 
| --- | --- | --- | 
| LI | LI | Shared tenancy | 
| LI | BYOL | Shared tenancy or Dedicated Hosts | 
| BYOL | BYOL | Dedicated Hosts | 
| BYOL | LI | Not supported | 

## Configuring machine specifications<a name="estimate-workload-configure"></a>

Based on your choice of machine specification, we recommend the Amazon EC2 instance that AWS Pricing Calculator uses to generate an estimate for your cost\. You can also select different instances than the one recommended, or add multiple machine specifications for a workload\.

This section defines the terms mentioned in the **Configure machine specifications** section\.

****Machine description****  
A description for the machine\. This is generally a hostname identifier\. If unknown, you can specify unique software components running on this machine—for example, `WebApp DB1` or `Webserver 1`\.

****Operating system****  
You can choose an operating system with a licensing option, depending on your tenancy qualification\. The default value is `Windows`\.

****SQL Server edition****  
You can choose a SQL Server with licensing option, depending on your tenancy qualification\. The default value is `SQL Standard`\.

****Storage volumes per specification****  
You can specify the storage needs in this section\. If you don't know storage needs upfront, you can remove it from the estimate using **Remove**\. This section is optional\.  
Instances can have either none or one or more storage volumes associated\. Choose **Add new volume** to add multiple volumes to an instance\.  
You can use different volume types for each volume\. The calculator recommends the appropriate Amazon EBS storage type based on the optional inputs such as **IOPS** and **Throughput**\.    
****Storage amount****  
You can specify your storage amount needs\. The default value is 1000 GB\. If only storage amount is specified, the default recommended Amazon EBS storage type is `General Purpose SSD (gp3)`\.  
****IOPs****  
IOPS \(input/output operations per second\) is the standard unit of measurement for the maximum number of reads and writes to non\-contiguous storage locations\. IOPS describes performance in solid state drives \(SSD\), hard disk drives \(HDD\), and storage area networks\.  
You can specify IOPs for I/O intensive workloads\. AWS uses this value to potentially recommend `io2` Amazon EBS storage types\.  
`io2` delivers a consistent baseline performance of up to 500 IOPS/GB to a maximum of 64,000 IOPS,\. It provides up to 1,000 MB/s of throughput per volume\.  
****Throughput****  
Throughput measures how many units of information a system can process in a period of time\. It can refer to the number of I/O operations per second, but is typically measured in bytes per second\.  
You can specify this input for throughput\-intensive workloads\.  
`st1` is backed by hard disk drives\. It's ideal for frequently accessed, throughput\-intensive workloads with large datasets and large I/O sizes\. Examples include MapReduce, Kafka, and log processing\.

****EC2 instance type****  
**Obtain an EC2 instance type recommendation**  
This is the default choice\. Choose the number of vCPUs and memory inputs to generate an EC2 instance recommendation\. Only x86 architecture instances are considered\. The default vCPU value is 4, and memory is 16 GB\.   
**Search for an EC2 instance type**  
You can use this option to choose different instance types than the recommended instance\.  
To find an instance, search by minimum requirements or by name\. Minimum requirements are the most useful when you know the specification of the instances you prefer\. Instance names are useful when you know the instance family or size of the instance you prefer\. For example, you can search for an instance with a minimum of 4 vCPUs and 16 GB memory, or for an m5 instance name\.  
You can also search instances by using filters such as *instance category*\. We recommend memory\-optimized instances for database workload\. You can search for them faster by using the instance category filter\.

****Optimize CPU****  
You have the flexibility of specifying a custom number of vCPUs while using the same memory, storage, and bandwidth of a full sized instance\. The default value is the same as the vCPU input specified for the machine specification\.  
For example, a x1e\.4xlarge instance currently offers 16 vCPU, by default\. However, you can specify x1e\.4xlarge with 4, 5, 6, 7, 8, 9,10, 12,14 Optimized vCPUs\. This means BYOL customers can optimize vCPU\-based licensing costs\. The CPU optimized instance has the same price as the instance that iisn't optimized for CPU\.

****Quantity****  
The default value is 1\. This is the minimum number required\.

****SQL passive node****  
A passive SQL Server node is one that's not serving SQL Server data to clients or running active SQL Server workloads\. If you select this check box and you bring SQL Server 2014 and later versions to AWS with Software Assurance, you aren't required to license SQL Server on a passive node\.

## Pricing strategy<a name="estimate-workload-pricing"></a>

Your choices in the **pricing strategy** section determine the pricing strategy AWS Pricing Calculator uses to generate your estimate\.

**Pricing model**  
The pricing model determines whether you're searching for a pay\-as\-you\-use instance or an instance that you can reserve in advance\. For Reserved Instance \(RI\) payment options, see **payment options**\.  
The default value is `Standard Reserved Instances`\. This is because it's the most common Amazon EC2 purchase, and it offers the flexibility with highest discount for most use cases\.

**Reservation term**  
You purchase a reservation for the period of your contract when you reserve an RI\. Choose either 1 or 3 years for your term\. The default is set to 1 year\. This is to save no costs\.

**Payment options**  
Payment options determine when you pay for your RI reservation\.  
**Full upfront** \- You pay for the entire reservation upfront, resulting in a single payment but no monthly, recurring payments\. This option provides the best discount\.  
**Partial upfront** \- You pay for a smaller, partial upfront fee along with monthly payments\.  
**No upfront** \- You only pay on a monthly basis\.  
The default value is **No upfront**\. It gives you the least costly start\-up price\.

## Cost details<a name="estimate-workload-cost"></a>

The cost details section provides details for your workload\.

**EC2 Instance costs**  
A summary of the itemized breakdown for an EC2 instance\. Pause on each row to show additional information, such as instance type, operating system, SQL version, vCPU, memory, quantity, optimize CPU, and SQL passive node\.

**Amazon EBS costs**  
The itemized cost breakdown for Amazon EBS\.

**SQL bring your own license summary**  
A summary to clarify the number of cores for your BYOL SQL Server licenses\.