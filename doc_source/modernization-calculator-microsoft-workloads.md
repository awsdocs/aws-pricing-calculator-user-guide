# Generating Microsoft workload estimates with AWS Modernization Calculator<a name="modernization-calculator-microsoft-workloads"></a>

AWS Modernization Calculator for Microsoft workloads provides a pricing estimate for modernizing your Microsoft workloads using open source and AWS cloud\-native services deployed on AWS\.

The calculator creates an estimate total cost of ownership for transforming your Windows and SQL server applications into a modern architecture\. To use the calculator, you don't need an AWS account\.

AWS Modernization Calculator for Microsoft workloads recommends modernized architecture for application patterns such as multi\-tier, batch processing, CI/CD, or containerization\. These recommendations are based on commonly adopted architectures by the AWS customer community\. The calculator offers a reliable way to get modernization cost estimates without in\-depth assessments\. Using this information, you can conduct an in\-depth assessment with Migration Hub Strategy Recommendations\. For more information, see [What is Migration Hub Strategy Recommendations?](https://docs.aws.amazon.com/migrationhub-strategy/latest/userguide/what-is-mhub-strategy.html)

You can create an estimate with AWS Modernization Calculator for Microsoft workloads at [https://modernization\.calculator\.aws/microsoft/workload](https://modernization.calculator.aws/microsoft/workload)\.

To save, export, and share your estimate, make selections and provide inputs in the four steps\.

**Topics**
+ [Step 1: Select current architecture pattern](#step1-pattern)
+ [Step 2: Select an architecture size](#step2-size)
+ [Step 3: Select modernized architecture pattern](#step3-architecture)
+ [Step 4: Edit service configuration](#step4-configuration)
+ [My Estimate](#estimate)

## Step 1: Select current architecture pattern<a name="step1-pattern"></a>

Provide details about the current architecture of your application in this step, and start creating your estimate\.

**New estimate**

Add a description for this estimate \(for example, *App1 modernization*\)\.

**Current application/workload location**

To specify the current location of where your application is deployed, select from AWS, on\-premises, or other cloud\.

**Architecture category**

Specify the architecture category of your application by choosing from architecture pattern, use case or custom\. The category selection provides further options to analyze your application\.
+ **Architecture pattern** refers to a fundamental schema for software systems in an organization\. It defines the structural composition of the program and the interactions between the elements\. In most enterprises, some of the commonly found patterns include the following\.
  + **Multi\-tier** pattern has been a cornerstone architecture pattern for decades, and remains a popular pattern for user\-facing applications\. Multi\-tier generally consists of a presentation tier, data tier, and logic tier\. These three tiers can be hosted on the same or separate servers\. This pattern provides a general framework to ensure decoupled and independently scalable application components can be separately developed, managed, and maintained\.
  + **Batch processing** is the method computers periodically use to complete high\-volume and repetitive data jobs\. Certain data processing tasks, such as backups, filtering, and sorting, can be compute intensive and inefficient to run on individual data transactions\. Instead, data systems process such tasks in batches\. These tasks are processed during off\-peak times such as the evening and overnight\.
+ **Use case** includes grouped architecture patterns\. This grouping represents a collaboration by different teams on performing tasks\. Use cases are further categorized into the following\.
  + **Software development** involves several steps including creating, testing, staging, and deploying software\. In an organization, multiple teams collaborate as a group to create software\.
  + **Container** provides a standard way to package your application's code, configurations, and dependencies into a single object\. Containers share an operating system that's installed on the server and run as resource\-isolated processes\. This ensures quick, reliable, and consistent deployments, regardless of the environment\. Containers are lightweight and provide a consistent and portable software environment for applications to run and scale virtually anywhere\. Building and deploying microservices, running batch jobs for machine learning applications, and moving existing applications into the cloud are some of common use cases\.
+ **Custom** category provides you with the option to build any custom architectures by selecting the relevant AWS services from the list\. This is a suitable option if you're familiar with AWS services and their role in your application's architecture pattern\.

## Step 2: Select an architecture size<a name="step2-size"></a>

This step includes a short questionnaire about the specifics of your application's architecture\. All questions are optional\. The calculator provides a sizing recommendation based on your answers\. The default recommendation is **Small**\.

If you choose to answer the questions, the calculator recommends a size\. You can proceed with the recommended size or select any size that meets your business requirements\.

## Step 3: Select modernized architecture pattern<a name="step3-architecture"></a>

In this step, the calculator provides modernized architecture pattern options based on your inputs in preceding steps\. You can download the pattern diagram to learn more\.

If you see more than one option, you can choose the recommended or another pattern\. If you have one recommendation without options, choose the recommended pattern to proceed to the next step\.

## Step 4: Edit service configuration<a name="step4-configuration"></a>

You can see a summary of recommendations in this step\. You can see a list of recommended AWS services\. You can add or remove any service, and change the recommended settings of each service\.
+ **AWS Region** has a drop\-down list that you can select the Region where you want to host your modernized application from\. The pricing of AWS services can differ by Region\.
+ **Estimated cost** provides the total monthly cost of running a modernized application on AWS\. The cost isn't intended as an actual price quote\. It doesn't account for data transfer charges or any additional configurations offered by AWS services\.
+ **AWS services** lists the recommended services for your modernized application\. You can add or delete any service from this list\. You can expand each service card to modify size and parameters for that service\. You can also see the breakdown of cost for each service by expanding *Show calculation*, which is located in each service card\.
+ Select **Save** to see a graphical presentation of estimate on **My Estimate** page\.

## My Estimate<a name="estimate"></a>

This page provides the estimate for your modernized application\. You can do the following with this page:
+ Clone the same or add new workload to your estimate\.
+ Increase or decrease the number of applications in a workload\.
+ Change the recommended AWS services by editing a workload\.
+ Add the cost of accessing AWS Support to your estimate\.
+ Export to an excel file or share your estimate by using a unique URL\.

*If you retrieve and modify a shared estimate, you must save and share the modified version\. The modifications aren't automatically added to your original estimate\.*