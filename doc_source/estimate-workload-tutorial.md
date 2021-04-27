# Tutorial: Using Windows Server and SQL Server on Amazon EC2 calculator<a name="estimate-workload-tutorial"></a>

This tutorial shows you how to use the Microsoft Windows Server and Microsoft SQL Server on the Amazon EC2 calculator to generate a pricing estimate\. 

To start pricing your workload, open the [AWS Pricing Calculator console](https://calculator.aws/#/createCalculator/EC2WinSQL), and navigate to **Configure Windows Server and SQL Server on Amazon EC2**\.

## What are your license options?<a name="estimate-workload-tutorial-license"></a>

AWS offers flexible cost optimizations so you have options that best fits your needs\. The following three types of licenses are offered:
+ Flexible pay\-as\-you\-go with License Included \(LI\)
+ Bring your Microsoft License Mobility benefits to AWS \(BYOL\)
+ Dedicated options for products without Microsoft License Mobility

## Example scenario table<a name="estimate-workload-tutorial-example"></a>

**Example**  
This example uses the following workload scenario to show several capabilities in the AWS Pricing Calculator\.  


| Host description | vCPUs | Ram | Storage \(GB\) | IOPS | Software | Optimize vCPUs | Quantity | Passive node count | 
| --- | --- | --- | --- | --- | --- | --- | --- | --- | 
| Server 1 | 16 | 800 | 5000 | 60000 | SQL Enterprise Edition | 16 | 10 | 5 | 
| Server 2 | 16 | 64 | 3000 | 15000 | SQL Standard Edition | 16 | 8 | 4 | 
| Server 3 | 8 | 16 | 1000 |  | SQL Web Edition | 8 | 10 | 0 | 
| Server 4 | 4 | 32 | 500 |  | Windows | N/A | 8 | N/A | 

Begin your estimate by naming your estimate and selecting your Region\.
+ Description: `Workload_SQL_BYOL`
+ Region: `US East (Ohio)`

  This is your AWS Region choice\. All AWS resources are priced based on your Region choice\.

**Topics**
+ [What are your license options?](#estimate-workload-tutorial-license)
+ [Example scenario table](#estimate-workload-tutorial-example)
+ [Step 1: Choose your licensing and tenancy recommendation](estimate-workload-tutorial-step1.md)
+ [Step 2: Configure your machine specifications](estimate-workload-tutorial-step2.md)
+ [Step 3: Choose a pricing strategy](estimate-workload-tutorial-step3.md)
+ [Step 4: Show calculation and cost details](estimate-workload-tutorial-step4.md)
+ [Step 5: View and add a Windows Server and SQL Server on Amazon EC2 estimate](estimate-workload-tutorial-step5.md)