# Create an estimate, configure a service, add more services, edit your inputs, and generate bulk estimates<a name="create-estimate"></a>

When you generate an estimate, you can either add services directly to your estimate or create a group and add the services to your group\. This section shows how to set up a group with an Amazon EC2 instance that you can use to perform tasks such as run a small program or host a website\. To get started, create your estimate using the following steps\.<a name="create-estimate-process"></a>

**To create your estimate**

1. Open AWS Pricing Calculator at [https://calculator\.aws/\#/](https://calculator.aws/#/)\.

1. Choose **Create estimate**\.

1. On the **Add service** page, find the service that you want to choose and then choose **Configure**\. For more information, see [Configure a service](#configure-service)\.

1. Add a **Description** for the estimated service\.

1. Choose a **Location type**\.

1. Choose a **Region**\.

1. Enter your values to configure a service estimate\.

1. \(Optional\) To add more services to your estimate, choose **Save and add service**\.

1. Choose **Save and view summary** to view your estimate details\.

## Configure a service<a name="configure-service"></a>

This section shows how to configure a service you're creating an estimate for\. In this example, we're adding an Amazon EC2 instance\.<a name="generate-quick-estimate"></a>

**To configure a service for your estimate**

1. Open the **Add service** page at [https://calculator\.aws/\#/addService](https://calculator.aws/#/addService) \.

1. Enter **Amazon EC2** in the search bar and choose **Configure**\.

1. In the **Description** field, enter a description for your estimate\.

1. Choose a **Location type**\.

1. Choose a **Region**\.

1. The calculator view is preloaded with default values, so you can see a starting estimate without adding or changing any information\. You can change any of the values for the following parameters\. Otherwise, you can also keep the defaults when they're applicable\.
   + Tenancy
   + Operating system
   + Workloads
   + The number of Amazon EC2 instances
   + Amazon EC2 instance: Search by instance name, or by filters \(Instance family, vCPU, Memory, Network performance\)
   + The pricing options
   + The reservation term
   + The payment options

1. \(Optional\) Choose **Show calculations** to view the calculations behind your estimate\.

1. \(Optional\) In the **Amazon EBS** section, choose the storage for each Amazon EC2 instance, and enter the storage amount\.

   If you aren't adding Amazon EBS volumes, enter **0**\.

1. \(Optional\) In the **Detailed monitoring** section, select the checkbox to turn on detailed monitoring for your instance\.

1. \(Optional\) In the **Data transfer** section, enter the data you expect to transfer in and out of Amazon EC2\.

1. \(Optional\) Use the **Elastic IPs** calculator to estimate costs for elastic IP addresses\.

1. \(Optional\) In the **Additional costs** section, enter any necessary costs to add to your estimate\.

1. \(Optional\) To add more services to your estimate, choose **Save and add service**\.

1. Choose **Save and view summary** to view your estimate details\.

## \(Optional\) Add a group<a name="add-group"></a>

Use groups to organize services together\. You can add one or more services to each group\. You can also use groups to organize your estimate in different ways\. For example, you can organize it by cost center, service stack, product architecture, or client\.

For more information about groups, see [Using groups to organize your estimates](estimate-groups.md)\.<a name="add-group-process"></a>

**To add a group to your estimate**

1. Open the **My estimate** page at [https://calculator\.aws/\#/estimate](https://calculator.aws/#/estimate) \.

1. Choose **Create group**\.

1. Enter a group name\.

1. Choose **Create group**\.

## Add more services<a name="Add-more"></a>

You can add more services to generate a complete estimate for your architecture\. For process examples and tutorials that show estimates for specific services, see [Estimate examples for services](estimate-examples.md)\.<a name="add-more-process"></a>

**To add more services to your estimate**

1. Open the **My estimate** page at [https://calculator\.aws/\#/estimate](https://calculator.aws/#/estimate) \.

1. Choose a group from the left panel to add your service to\.

1. Choose **Add service**\.

1. Search for a service and choose **Configure**\.

1. Enter your values to configure a service estimate\.

1. \(Optional\) To add more services to your estimate, choose **Save and add service**\.

1. Choose **Save and view summary** to view your estimate details\.

1. Repeat as needed\.

## Edit your inputs<a name="update-inputs"></a>

You can edit the inputs for a service added to your estimate\.<a name="update-inputs-process"></a>

**To edit the inputs for a service**

1. Open the **My estimate** page at [https://calculator\.aws/\#/estimate](https://calculator.aws/#/estimate) \.

1. Under the **My Estimate** section, locate the service you want to update and choose the **Edit** icon\.

1. Edit your changes and choose **Update** to return to your **My Estimate** page\.

## Generate bulk estimates<a name="bulk-estimates"></a>

You can use the bulk import feature in the AWS Pricing Calculator to estimate multiple input configurations of Amazon EC2 instances and Amazon EBS volumes\. Use an Excel template to upload your bulk inputs\.

**Note**  
You can enter input configurations up to 1,000 rows with each bulk upload\.<a name="bulk-estimates-process"></a>

**To generate a bulk estimate**

1. Open AWS Pricing Calculator at [https://calculator\.aws/\#/](https://calculator.aws/#/)\.

1. Choose **Create estimate**\.

1. Choose **Bulk import**\.

1. Choose a service you want the bulk estimate for\.

1. \(Optional\) Enter a group name to organize your estimates\.

1. In the **Download template** section, choose** Download Excel template**\. This downloads the Excel template file for the service you want the estimate for\.

1. Fill out the Excel template based on the instructions in the template file\. For more information about the column definitions for the Amazon EC2 template, see [Input column definitions for the Amazon EC2 instances template](#bulk-estimates-EC2-input)\.

1. In the **Upload the Excel file** section, upload your Excel file\.

   Your input parameters are validated once you upload your file\. If any of your input configurations aren't successfully validated, choose **View Errors** to view and download the list of errors\. The downloaded file provides the error details for each row in your file\.

   Once your errors are fixed, upload the template again\.

1. Choose **Save and view summary** to view your estimate summary\. The estimate summary includes the estimates for each input row that validated successfully\.

1. Choose **Save and add service** to add more services to your estimate\.

### Input column definitions for the Amazon EC2 instances template<a name="bulk-estimates-EC2-input"></a>

This list defines the columns needed for the Amazon EC2 bulk input estimate\.

**Group**  
Define the groups to organize your estimates\. The group name can only be an alphanumeric string, and can't contain special characters `>`, `<`, and `&`\. For more information, see [Using groups to organize your estimates](estimate-groups.md)\.  
Example: **Beta**  
Required: No

**Description**  
Enter a description for your estimate\. The group name can only be an alphanumeric string, and can't contain special characters `>`, `<`, and `&`\.  
Example: **windows estimate**  
Required: No

**AWS Region**  
Enter the AWS Region you want to estimate the Amazon EC2 instance prices for\. Use the [Amazon EC2 Pricing Calculator](https://calculator.aws/#/addService/EC2) to check for available Region codes and the associated Region names\.  
Example: **us\-east\-1**  
Required: Yes

**Operating system**  
Choose the operating system to run your Amazon EC2 instances on\.  
Example: **Linux**  
Required: Yes

**Instance type**  
Enter the Amazon EC2 instance name you'd like the estimate for\. Use the [Amazon EC2 Pricing Calculator](https://calculator.aws/#/addService/EC2) and [Amazon EC2 Pricing pages](http://aws.amazon.com/ec2/pricing/) to see the available Amazon EC2 instance names for the `Region` and `Operating system` you choose\.  
Example: **a1\.medium**  
Required: Yes

**Tenancy**  
Choose the tenancy to run your Amazon EC2 instances on\.  
Example: **Shared instances**  
Required: Yes

**Number of instances**  
Enter the number of Amazon EC2 instances you need for your estimate\.  
Example: **10**  
Required: Yes

**Assumed usage**  
Enter the expected usage of your Amazon EC2 instances\. This field is only applicable when the usage type you choose is `Hours per week`\.  
Example: **10**  
Required: Yes

**Usage type**  
Choose the usage type based on your workload\.  
Example: **Hours**, **Week**  
Required: Yes

**Purchase options**  
Choose your pricing option\.  
Example: **1 Yr No Upfront Compute Savings Plan**  
Required: Yes

**Storage type**  
Choose the Amazon EBS volume storage type\.  
Example: **General Purpose SSD \(gp2\)**  
Required: No

**Storage amount per instance**  
Enter your storage amount in GB per instance\.  
Example: **12**  
Required: No

**Provisioning IOPS per instance**  
Enter the provisioning IOPS per volume\. This is applicable when your chosen storage type is `General Purpose SSD (gp3)`, `Provisioned IOPS SSD (io1)`, or `Provisioned IOPS SSD (io2)`\.  
Example: **1000**  
Required: No

**EBS throughput per instance **  
Enter the throughput per volume in MBps only\. This is applicable when storage type selected is `General Purpose SSD (gp3)`\.  
Example: **50**  
Required: No

**Snapshot frequency**  
Choose the snapshot frequency\.  
Example: **Daily**  
Required: No

**EBS snapshot per instance **  
Enter the amount changed per snapshot in GB only\.  
Example: **100**  
Required: No