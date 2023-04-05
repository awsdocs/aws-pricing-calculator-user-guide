# Generating Amazon Elastic Compute Cloud \(Amazon EC2\) estimates<a name="ec2-estimates"></a>

You can use the Amazon EC2 pricing calculator to estimate costs for Amazon EC2 instances and dedicated hosts\.<a name="ec2-estimates-process"></a>

**To start an Amazon EC2 estimate**



1. Open the **Amazon EC2 estimate** page at [https://calculator\.aws/\#/createCalculator/EC2](https://calculator.aws/#/createCalculator/EC2) \.

1. Enter the description for your Amazon EC2 estimate\.

1. Choose the **Location type** and **Region** from the dropdown\.

The calculator view is preloaded with default values so you can see a starting estimate without adding or changing any information\. You can change any of the values for the following parameters\. Otherwise, you can also keep the defaults when they're applicable\.

The Amazon EC2 instance estimate path has the following sections and parameters:

**Topics**
+ [Amazon EC2 instance specifications](#quick-ec2-specifications)
+ [Pricing options](#quick-pricing-strategy)
+ [Adding an Amazon EBS estimate](#quick-ebs)
+ [Adding detailed monitoring costs](#ec2-detailed-monitoring)
+ [Adding data transfer estimates](#ec2-data-estimates)
+ [Adding Elastic IP costs](#ec2-elastic)
+ [Adding additional costs](#ec2-additional-costs)

**Note**  
For a tutorial on how to generate an Amazon EC2 estimate, see [Getting started](getting-started.md)\.

## Amazon EC2 instance specifications<a name="quick-ec2-specifications"></a>

These settings determine the Amazon EC2 instance that AWS Pricing Calculator uses to generate an estimate for you\.

**Select your tenancy**  
The default value for tenancy is `Shared Instances`\.

**Select your operating system**  
The operating system on an Amazon EC2 instance\. AWS Pricing Calculator generates your estimate using Amazon Machine Images \(AMIs\) that match the OS you choose\. Choose the operating system \(OS\) that best matches your needs\. The default value for the OS is Linux\.

 **Choose your instance type**  
AWS Pricing Calculator lists all available instance types\. Use the search bar to filter the instances\.  
**Search for an instance type by name**  
If you know the instance family or instance size that you want, it's efficient to search for the instance name\. For example, you can search for a `t2.medium` instance\.  
**Search for an instance type based on minimum requirements**  
Minimum requirements are most useful when you know the specifications of the instances that you want\. For example, you can search either for an instance with a minimum of four vCPUs and 16 GB of memory for any network performance\.  
For information about the available Amazon EC2 instance families, see [Amazon EC2 Instance Types](http://aws.amazon.com/ec2/instance-types/)\.

**Number of EC2 instances**  
The default value is one\. AWS Pricing Calculator uses this default because it's the minimum number that you might need\.

**Workloads**  
Workloads are the usage patterns that match your Amazon EC2 usage\. Choosing the workload that most closely matches what you use reduces the number of On\-Demand and unused RI hours that you might purchase\. It does this by covering your usage with the most appropriate combination of RIs and On\-Demand Instances for you\. You can define more than one workload for your estimate\.  
**Constant usage**  
This workload is suitable for use cases that have a constant, predicable load\. This includes use cases such as logging traffic to a website or running processes in the background\.  
**Daily spike**  
This workload is best for usage patterns that peak once a day\. This is suitable for scenarios where, for example, you need to run several jobs at midnight or have a morning news spike\.  
**Weekly spike**  
This workload is best for patterns that peak once a week\. This is suitable for scenarios such as blogs that post once a week and weekly television shows\.  
**Monthly spike**  
This workload is best for traffic that spikes once a month, such as monthly invoices, payroll, or other monthly reports\.

## Pricing options<a name="quick-pricing-strategy"></a>

These settings determine the pricing strategy that AWS Pricing Calculator uses to generate your estimate\.

**Pricing model**  
The pricing model determines whether you're searching for a pay\-as\-you\-use instance or an instance that you can reserve in advance\. Reserving an instance isn't the same as paying for the use of an instance\.

**Reservation terms**  
When you reserve a Reserved Instance \(RI\), you purchase a reservation for the period of your contract\. Contracts can be for either one or three years\.  
The default value is one year\. AWS Pricing Calculator uses this default because it's the least costly option for trying out AWS\.

**Payment options**  
For RIs, payment options determine when you pay for your reservation\. You can pay for the entire reservation upfront, which is a hefty single\-time payment but you have no monthly payments\. You can pay for the RI with a partial upfront payment and a monthly payment\. This gives you a smaller upfront cost but accrues monthly costs\. You can also pay with no upfront payment\. This means you pay only on a monthly basis\. All upfront gives you the best discount, but no upfront and partial upfront spread your costs out over a greater period of time\.  
The default value for the payment options is `No Upfront`\. AWS Pricing Calculator uses this default because it gives you the least expensive start\-up price\.

**Expected utilization of EC2 instances**  
Enter the expected usage of Amazon EC2 instances\. The feature is only applicable when you select the On\-Demand pricing strategy\.

**Spot**  
The calculator shows the historical average discount percentage for the instance chosen\. You can enter a percentage discount for creating estimates\.

## Adding an Amazon EBS estimate<a name="quick-ebs"></a>

These settings determine the Amazon EBS settings that AWS Pricing Calculator uses to generate an estimate for you\. Amazon Elastic Block Store \(Amazon EBS\) is a type of storage that you can connect to your Amazon EC2 instance\. You can use it to do things such as backing up your instance, creating a boot volume, or running a database on your instance\. For more information about Amazon EBS, see the [Amazon Elastic Block Store documentation](https://docs.aws.amazon.com/AWSEC2/latest/UserGuide/AmazonEBS.html)\.

**Storage volume**  
The storage volume determines what kind of storage that Amazon EBS assigns to your instance\. Different types have different capabilities\. For example, you can choose better I/O and faster calculations, or slower, less expensive options for your specific use cases such as boot volumes and backups\.

**Storage amount**  
The storage amount determines how much storage your Amazon EBS volume has\.  
The default value is `30 GB`\. You can enter `0 GB` if you don't attach Amazon EBS volumes to your Amazon EC2 instance\. You can also estimate additional Amazon EBS volumes by configuring and adding a standalone Amazon EBS calculator into your estimate at [https://calculator\.aws/\#/createCalculator/EBS](https://calculator.aws/#/createCalculator/EBS) \.

## Adding detailed monitoring costs<a name="ec2-detailed-monitoring"></a>

Your instances are turned on for basic monitoring by default\. You can optionally turn on detailed monitoring\. Once detailed monitoring is turned on, the Amazon EC2 console shows monitoring graphs with a one minute period for the instance\. For more information, see [Detailed monitoring](https://docs.aws.amazon.com/AWSEC2/latest/UserGuide/using-cloudwatch-new.html)\.

## Adding data transfer estimates<a name="ec2-data-estimates"></a>

You can accrue additional costs by transferring data in and out of Amazon EC2\. If you know how much data you can expect to upload or download in a month, you can add these costs to your estimate\. For more information, see the [Data transfer](http://aws.amazon.com/ec2/pricing/on-demand/) section on the *On\-Demand Pricing * page\.

## Adding Elastic IP costs<a name="ec2-elastic"></a>

You can have one Elastic IP \(EIP\) address associated with a running instance at no charge\. If you associate additional EIPs with that instance, you will be charged for each additional EIP associated with that instance per hour on a pro rata basis\. A small hourly charge applies when EIPs are not associated with a running instance or when they are associated with a stopped instance or unattached network interface\. For more information, see [Elastic IP Addresses](http://aws.amazon.com/ec2/pricing/on-demand/) section on the *On\-Demand Pricing * page\.

## Adding additional costs<a name="ec2-additional-costs"></a>

You can add a custom cost to your Amazon EC2 pricing estimates\. You can use this to add any placeholder costs you'd like to include in your estimates\.