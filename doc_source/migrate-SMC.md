# Migrating from Simple Monthly Calculator estimates to the AWS Pricing Calculator<a name="migrate-SMC"></a>

**Important**  
Simple Monthly Calculator \(SMC\) reaches its end of standard support on March 31, 2023 at 11:59 PM PST\. You cannot create new estimates in SMC after this date\. You can convert your saved SMC estimates to AWS Pricing Calculator using the steps outlined in this section\. This conversion feature closes on December 31, 2023 at 11\.59PM PST\.   
If you have existing SMC estimates, we recommend that you migrate to the AWS Pricing Calculator using the conversion feature at your earliest convenience\. If you don't need access to your saved SMC estimates, no action is needed\.

**To convert your SMC estimate to an estimate compatible with AWS Pricing Calculator**

1. Copy and paste your unique SMC estimate link into your browser\. You can view the status of your estimate conversion in the **Save and Share** dialog box\.

1. Choose **Copy link** to copy the URL of the of the estimate generated in AWS Pricing Calculator\.

1. \(Optional\) If your SMC estimate isn't successfully generating in AWS Pricing Calculator, choose **View details** to see the reasons why the conversions weren't successful\.

1. Choose **OK**\.

1. Copy and paste your generated AWS Pricing Calculator \(in step 2\) into your browser\.

1. Save the generated link from your AWS Pricing Calculator to access your estimate at a later time\.

## Differences between Simple Monthly Calculator and AWS Pricing Calculator estimates<a name="migrate-SMC-differences"></a>

There are several reasons why your SMC estimate and your AWS Pricing Calculator estimates don't match in total costs\.
+ **AWS Free Tier pricing**: The AWS Pricing Calculator doesn't account for Free Tier pricing in cost calculations\.
+ **Time period**: The AWS Pricing Calculator calculates using 730 hours in a month for cost calculations\. This is based on the calculation, 365 days a year x 24 hours a day for 12 months a year\.

### Services and features not supported by AWS Pricing Calculator<a name="migrate-SMC-notsupported"></a>

You might have Simple Monthly Calculator estimates saved previously that won't successfully migrate to AWS Pricing Calculator\. This is because some services and features aren't supported in AWS Pricing Calculator at this time\. The following table outlines what is currently not supported in AWS Pricing Calculator\.


| Service name | Pricing feature not supported in AWS Pricing Calculator | 
| --- | --- | 
|  Amazon EC2  |  Additional `T2/T3/T4g` Unlimited vCpu Hours Legacy Amazon EC2 instances and instance families  | 
|  Amazon S3  |  Transfer acceleration Glacier select Cross region replication  | 
| Amazon CloudFront | HTTP requests Invalidation requests SSL certificates | 
| Amazon RDS | RDS Aurora Global Database | 
| Amazon DynamoDB | Global tables | 
| Amazon CloudWatch | Archived logs Metric streams | 
| Amazon Redshift | Previous generation node type | 
| Amazon S3 Glacier | Glacier select | 
| Amazon CloudSearch | Entire service | 
| Amazon SimpleDB | Entire service | 
| AWS Key Management Service | Customer managed keys \(CMK\) \- multi Region  | 

**Note**  
You must generate new AWS Pricing Calculator sharable links if you make changes to your estimate\. For more information, see [Sharing your estimate](save-share-estimate.md)\.