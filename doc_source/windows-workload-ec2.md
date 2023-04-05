# Generating Windows Server and SQL Server estimates on Amazon EC2 Dedicated Hosts<a name="windows-workload-ec2"></a>

You can use the workload calculator in AWS Pricing Calculator as a guide to the AWS tenancy qualifications for Microsoft Windows Server and SQL Server on Amazon Elastic Compute Cloud \(Amazon EC2\)\. You can use the workload calculator to estimate AWS cost using minimal information or generate a rough estimate\.

For options for using Microsoft software licenses on the AWS Cloud, see [Microsoft Licensing on AWS](http://aws.amazon.com/windows/resources/licensing/)\.

**To generate an estimate for Windows Server and SQL Server on Amazon EC2**

1. Open AWS Pricing Calculator at [https://calculator\.aws/\#/](https://calculator.aws/#/)\.

1. Choose **Create estimate**\.

1. Do one of the following:
   + Under **Windows Server and SQL Server on Amazon EC2**, choose **Configure**\.
   + Search for **Windows Server and SQL Server on Amazon EC2** from the **Find service** search bar\.

1. On the **Configure Windows Server and SQL Server on Amazon EC2** page, choose your customized settings\.
   + For information about your tenancy choices, see [Licensing and tenancy recommendations](windows-workload-estimates.md#estimate-workload-tenancy)\.
   + For instructions on how to choose your machine specifications, see [Configuring machine specifications](windows-workload-estimates.md#estimate-workload-configure)\.
   + For instructions on how to choose your pricing strategy, see [Pricing strategy](windows-workload-estimates.md#estimate-workload-pricing)\.
   + For instructions on how to choose your cost details, see [Cost details](windows-workload-estimates.md#estimate-workload-cost)\.

1. Choose **Save and add service** or **Save and view summary**\.

**Topics**
+ [Licensing and tenancy recommendations](#estimate-workload-tenancy-ec2)
+ [Input using bulk upload](#estimate-bulk-upload-ec2)
+ [Configuring machine specifications](#estimate-workload-configure-ec2)
+ [Review dedicated hosts](#estimate-dedicatedhost-ec2)
+ [Pricing strategy](#estimate-workload-pricing-ec2)

## Licensing and tenancy recommendations<a name="estimate-workload-tenancy-ec2"></a>

You can determine your AWS licensing and tenancy options for your workload through your choices for Windows Server and SQL Server licensing inputs\. The licensing options include AWS provided licenses with License Included \(LI\) offerings\. They also include your existing licenses with Bring Your Own License \(BYOL\) offerings for optimal cost savings\. You can identify which is the most suitable cloud tenancy\.


**AWS licensing and tenancy scenarios supported by AWS Pricing Calculator**  

| Windows Server | SQL Server | AWS tenancy | 
| --- | --- | --- | 
| LI | LI | Shared tenancy | 
| LI | BYOL | Shared tenancy or Dedicated Hosts | 
| BYOL | BYOL | Dedicated Hosts | 
| BYOL | LI | Not supported | 

## Input using bulk upload<a name="estimate-bulk-upload-ec2"></a>

You can use bulk upload to upload your machine configuration, operating system, SQL server edition, quantity, vCPU, and memory in an excel file\. Batch upload uploads this excel file to the AWS Pricing Calculator\. To do this, use the provided excel template worksheet\.

**To download the excel worksheet template**

1. Open AWS Pricing Calculator at [https://calculator\.aws/\#/](https://calculator.aws/#/)\.

1. Choose **Create estimate**\.

1. Do one of the following:
   + Under **Windows Server and SQL Server on Amazon EC2**, choose **Configure**\.
   + Search for **Windows Server and SQL Server on Amazon EC2** from the **Find service** search bar\.

1. On the **Configure Windows Server and SQL Server on Amazon EC2** page under the **Bulk upload instructions** sections, choose **Download template**\.

   For more information, see [Configuring machine specifications](#estimate-workload-configure-ec2)\.

1. Navigate to the downloaded file on your local machine\.
**Important**  
Don't remove any columns from the template\.  
Don't add any columns to the template\.  
Don't change the position of the template worksheet\.
**Tip**  
You can refer to the **Example** worksheet in the spreadsheet for an example data\.

1. Choose **Upload file**\.

1. Under the **Machine specifications** table, see the **Status** column to confirm if your template was uploaded correctly\.
   + **Accepted** \- The data that you entered is in the correct format\. The data can be used for providing recommendations\.
   + **Declined** \- The data format isn't valid\. You can see the upload fail reason from the same column\. After you correct your file, upload again using the previous steps\.

     If the declined fail reasons aren't addressed, these rows aren't included for recommendations on dedicated Hosts in the **Review dedicated hosts** table\.

1. Use the Review dedicated hosts section to see details such as host family, host description, instances, license count, and used capacity\. For more information, see [Review dedicated hosts](#estimate-dedicatedhost-ec2)\.

1. Use the Dedicated Host costs section to see details for your workload\.

   The costs table provides an itemized breakdown of the dedicated hosts with hourly cost, monthly cost per unit, and cost for the first twelve months included\. All costs are shown in USD currency\.

1. Use the **License\(s\) summary** section to clarify the list of licenses that you need to bring to AWS for the recommended dedicated hosts\.

1. Choose **Save and add service** to save your estimate prices, and add additional services to the AWS Pricing Calculator\.

## Configuring machine specifications<a name="estimate-workload-configure-ec2"></a>

Based on your choice of machine specification, we recommend that you select the Amazon EC2 instance that AWS Pricing Calculator uses to generate an estimate for your cost\. You can also select another instance or instances of your choosing or add multiple machine specifications for a workload\.

This section defines the terms that are mentioned in the **Configure machine specifications** section\.

****Machine description****  
A description for the machine\. This is generally a hostname identifier\. If you don't know the hostname identifier, specify unique software components that run on this machine—for example, `WebApp DB1` or `Webserver 1`\.

****Operating system****  
Depending on your tenancy qualification, you can choose an operating system with a licensing option\. The default value is `Windows`\.

****SQL Server edition****  
Depending on your tenancy qualification, you can choose a SQL Server with licensing option\. The default value is `SQL Standard`\.

****vCPU, Memory****  
Enter the number of vCPUs and memory inputs for your machine configuration\. For example, 4vCPU and 8GB of memory\.

****Quantity****  
The default value is 1\. This is the minimum number that's required\.

## Review dedicated hosts<a name="estimate-dedicatedhost-ec2"></a>

The **Review dedicated hosts** table shows your recommended dedicated hosts instance family based on your inputs\. You can see details such as host family and description, instances, license count, and used capacity \(virtual cores\)\. List count shows the license needed for a specific dedicated host\.

Choose the instances to see the machines that are optimally packed within a single dedicated host\.

By choosing **Download CSV**, you can download the dedicated host, instance, and license information\.

## Pricing strategy<a name="estimate-workload-pricing-ec2"></a>

Your choices in the **pricing strategy** section determine the pricing strategy that AWS Pricing Calculator uses to generate your estimate\.

**Pricing model**  
The pricing model determines whether you're searching for a pay\-as\-you\-use instance or an instance that you can reserve in advance\. For Reserved Instance \(RI\) payment options, see **payment options**\.  
The default value is `Standard Reserved Instances`\. This is because it's the most common Amazon EC2 purchase, and it offers the flexibility with highest discount for most use cases\.

**Reservation term**  
When you reserve an RI, you purchase a reservation for the period of your contract\. For your contract term, choose 1 year or 3 years\. By default, a term is 1 year\. This is to save costs\.

**Payment options**  
Payment options determine when you pay for your RI reservation\.  
**Full upfront** \- You pay for the entire reservation upfront, resulting in a single payment but no monthly, recurring payments\. This option provides the best discount\.  
**Partial upfront** \- You pay for a smaller, partial upfront fee along with monthly payments\.  
**No upfront** \- You only pay on a monthly basis\.  
The default value is **No upfront**\. It gives you the least costly start\-up price\.