# Step 5: View and add a Windows Server and SQL Server on Amazon EC2 estimate<a name="estimate-workload-tutorial-step5"></a>

In this step of the tutorial, you see a total monthly cost for all four workloads\. 

In the [AWS Pricing Calculator console](https://calculator.aws/#/createCalculator/EC2WinSQL), choose **Add to my estimate** to be directed to your **My estimate** page\. On your **My estimate** page, you can view your annual total\. Here, you have the option to choose **Save and share** to generate a public URL for your estimate\.

At this point, you successfully estimated workload costs for Windows Server License Included \(LI\) and SQL Server Bring Your Own License \(BYOL\) licensing\. You can clone your existing estimate to generate an estimate for the LI option for SQL Server\.

1. In the **Services** section, choose **Action**, and then choose **Clone service**\.

1. Choose **Edit** on the cloned estimate\.

1. For the description, enter **Workload\_LI**\.

1. Keep the **Region** as is\.

1. In the **Licensing and tenancy recommendation** section, keep the **Windows Server** and **SQL Server** check boxes cleared\.  
![\[Console screenshot that shows the Licensing and tenancy recommendation section.\]](http://docs.aws.amazon.com/pricing-calculator/latest/userguide/images/t9_workload_li.png)

1. For the SQL Server section, review and adjust the machine specifications\.

1. Review the new monthly cost estimate and aggregated monthly costs\.

1. Choose **Save**\.

On the** My Estimate** page, you can now compare the price under both the licensing options\. In this example, the shared tenancy with Windows LI and SQL Server BYOL option is approximately half of the cost of shared tenancy with Windows LI and SQL Server LI\.

We offer several cost saving programs that can lower the price of running your Windows workloads on Amazon Web Services\. For more information, choose **Learn more**\.

![\[Console screenshot that shows the My Estimate page with price comparisons for different licensing options.\]](http://docs.aws.amazon.com/pricing-calculator/latest/userguide/images/t10_compare_learnmore.png)

You now completed the tutorial for using the Microsoft Windows Server and Microsoft SQL Server to generate a pricing estimate\.