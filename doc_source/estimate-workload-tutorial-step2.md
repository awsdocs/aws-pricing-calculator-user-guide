# Step 2: Configure your machine specifications<a name="estimate-workload-tutorial-step2"></a>

In this step, you provide machine specifications from the [Example scenario table](estimate-workload-tutorial.md#estimate-workload-tutorial-example) to configure your specifications in AWS Pricing Calculator\. You enter the machine specs under **Configure machine specifications**\.

**To specify your machine specifications for this example**

1. In the [AWS Pricing Calculator console](https://calculator.aws/#/createCalculator/EC2WinSQL), for **Machine description**, keep the name as **Server 1**\.

1. For **Operating system**, choose **Windows Server**\.

1. For **SQL Server edition \(BYOL\)**, choose **SQL Server Enterprise**\.

1. Under **Storage volumes per specifications**, enter the storage amount \(GiB\) as **5000**, and **IOPS** as **60000**\. For more information, see [Machine specifications details](#estimate-workload-tutorial-step2-machinedetails)\.

1. For **Amazon EC2 instance type**, choose the AWS instance recommendation\. For more information, see [Amazon EC2 instance type details](#estimate-workload-tutorial-step2-ec2details)\.

1. For **Optimize vCPU**, keep the optimize CPU value as `16`\. For more information, see [Benefits of Optimize vCPUs](#estimate-workload-tutorial-step2-optcpudetails)\.

1. For **Quantity**, enter **10**\.

1. For number of passive instances, choose **5**\. 

1. Choose **Add machine** to add more machine specification types\. For this example, add the remaining three workloads from the [Example scenario table](estimate-workload-tutorial.md#estimate-workload-tutorial-example)\.

## Machine specifications details<a name="estimate-workload-tutorial-step2-machinedetails"></a>

If you enter the storage size \(GB\) only, the calculator provides you with the most cost\-effective Amazon Elastic Block Store \(Amazon EBS\) storage option\. If you enter a value between **16000** and **64000** for IOPS, the AWS Pricing Calculator recommends the io2 EBS volume type\. Anything value beyond that range, AWS Pricing Calculator recommends io2 Block Express with tiered pricing\. For more information, see [Amazon EBS volume types](https://docs.aws.amazon.com/AWSEC2/latest/UserGuide/ebs-volume-types.html)\.

![\[Console screenshot that shows the Machine specification details section that's used to configure your machine specs.\]](http://docs.aws.amazon.com/pricing-calculator/latest/userguide/images/t3_machine_specl.png)

## Amazon EC2 instance type details<a name="estimate-workload-tutorial-step2-ec2details"></a>

You can choose **Obtain an Amazon EC2 instance type recommendation** for the server type specifications\. AWS recommendations always default to the latest, cost\-optimized instances for Windows Server and SQL Server workloads\.

![\[Console screenshot that shows the recommended EC2 instance type.\]](http://docs.aws.amazon.com/pricing-calculator/latest/userguide/images/t4_instance_recommendations.png)

You can also choose **Search** for an Amazon EC2 instance type if you want the ability to filter the instance types\. You can filter by instance category, memory, CPU, and other options\.

![\[Console screenshot that shows how to search for an EC2 instance type in the list of instances.\]](http://docs.aws.amazon.com/pricing-calculator/latest/userguide/images/t5_search_instance.png)

## Benefits of Optimize vCPUs<a name="estimate-workload-tutorial-step2-optcpudetails"></a>

You have the flexibility to specify a custom number of vCPUs while using the same memory, storage, and bandwidth of a full\-sized instance\. This means that BYOL customers can optimize vCPU\-based licensing costs\. 

Even though the CPU optimized instance has the same price as the instance that's not optimized for CPU, it offers flexibility to choose the CPU count, so you can bring the right SQL Server license to avoid extra costs\. For example, an `x1e.8xlarge` instance has 32 vCPUs by default\. But you can specify `x1e.8xlarge` with Optimize CPU value to 16, 14, or 12\. 

The passive SQL Server nodes allow for additional cost optimization\. A passive SQL Server node doesn't serve SQL Server data or run active SQL Server workloads\. If you bring SQL Server to AWS with Software Assurance, you aren’t required to license SQL Server on a passive node\. 