# Step 1: Choose your licensing and tenancy recommendation<a name="estimate-workload-tutorial-step1"></a>

The AWS Pricing Calculator includes a licensing and tenancy recommendations section\. This section of the calculator simplifies the complex Windows Server and SQL Server licensing rules into several inputs\. It also recommends an AWS tenancy for your workload\. In this section, you enter your license details to determine your cost\-optimized tenancy qualifications\. For more information, see [Licensing and tenancy recommendations](windows-workload-estimates.md#estimate-workload-tenancy)\.

Some variables include the following:
+ Whether your Windows Server license was purchased before or after October 1, 2019
+ Whether your SQL Server license was purchased before or after October 1, 2019
+ Whether you want to bring your own license \(BYOL\), or you have active Software Assurance for SQL Server licenses

If you don’t choose a preference for Windows Server or SQL Server, the calculator assumes the Licence Included \(LI\) scenario that doesn't utilize the existing licenses for cost savings\.

![\[Console screenshot that shows the Licensing and tenancy recommendation section with a recommendation of EC2 dedicated hosts.\]](http://docs.aws.amazon.com/pricing-calculator/latest/userguide/images/t1_licensing_options.png)

**Example**  
This example uses the following options:  
+ Microsoft Windows Server License Included
+ Microsoft SQL Server BYOL

  For SQL Server BYOL, you must have active Microsoft Software Assurance associated with it\.

**To determine your licensing and tenancy recommendations for this example**

1. In the [AWS Pricing Calculator console](https://calculator.aws/#/createCalculator/EC2WinSQL), clear the **Windows Server** check box\.

1. Under **SQL Server**, select both options \(the estimate for Windows LI and SQL BYOL licensing model\)\.

1. Keep the default selection of the shared tenancy\.

   You will notice that the recommended tenancy options are **Shared** and **Dedicated Hosts**\. You can use the [Amazon EC2 Dedicated Hosts calculator](https://calculator.aws/#/EC2DedicatedHosts) to estimate Dedicated Host tenancy\.

![\[Console screenshot that shows the Licensing and tenancy recommendation section with Amazon EC2 shared tenancy selected.\]](http://docs.aws.amazon.com/pricing-calculator/latest/userguide/images/t2_licensing_options_win_byol_sql.png)