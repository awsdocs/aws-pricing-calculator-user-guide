# Getting Started<a name="getting-started"></a>

The Getting Started chapter walks you through a task using AWS Pricing Calculator so that you can get an idea of how to use AWS Pricing Calculator\. In this case, we walk you through getting an estimate for an Amazon EC2 instance using the Amazon EC2 **Quick estimate** option\. The Amazon EC2 quick estimate enables you to add an Amazon EC2 instance to your estimate without delving deeply into the different Amazon EC2 options\. This enables you to get an estimate without knowing the technical details of all of the Amazon EC2 instance types\.

**Topics**
+ [Overview](#overview)
+ [Prerequisites](#prereqs)
+ [Step 1: Create an Estimate](#step-1)
+ [Step 2: \(Optional\) Add a Group](#step-2)
+ [Step 3: Add and Configure a Service](#step-3)

## Overview<a name="overview"></a>

 When you generate an estimate you can either add services directly to your estimate or create a group and add the services to your group\.

This tutorial guides you through setting up a group with an Amazon EC2 instance that you can use to perform tasks such as run a small program or host a website\. If you don't want to create a group, skip [Step 2: \(Optional\) Add a Group](#step-2)\.

### Tasks<a name="overview-tasks"></a>

To complete this tutorial, perform the following tasks:

1. [Step 1: Create an Estimate](#step-1)

1. [Step 2: \(Optional\) Add a Group](#step-2)

1. [Step 3: Add and Configure a Service](#step-3)

## Prerequisites<a name="prereqs"></a>

This tutorial doesn't require any initial setup\. You can use it without an AWS account and without committing to anything\. 

## Step 1: Create an Estimate<a name="step-1"></a>

To get started generating an estimate, create your estimate and assign your estimate a Region\. <a name="create-estimate"></a>

**To create your estimate**

1. Open AWS Pricing Calculator at [https://calculator\.aws/\#/](https://calculator.aws/#/)\.

1. Choose **Create estimate**\.

1. On the **Create estimate** page, for **Estimate name**, enter a name for your estimate\.

1. For **Estimate Region**, choose a Region for your estimate\. You can add services for other Regions later\.

1. Choose **Create estimate**\.

## Step 2: \(Optional\) Add a Group<a name="step-2"></a>

A group is assigned to a single Region and enables you to organize services together for that Region\. You can have multiple groups that are associated with the same Region\. You can add one or more services to each group\. Different Regions might have different services available for you to use because not all AWS services are available for all Regions\. You can use groups to organize your estimate in different ways, such as by cost center, service stack, product architecture, or client\.<a name="add-group"></a>

**To add a group to your estimate**

1. To create a group, in the upper\-right header, choose **Add group**\.

1. For **Group name**, enter *My service group*\. 

1. For **Group Region**, choose a Region for your group\.

1. Choose **Add group**\.

## Step 3: Add and Configure a Service<a name="step-3"></a>

After you have an estimate and \(optionally\) a group, add and configure services to your estimate to generate estimated costs\. If you didn't create a group, use the **My estimate** view instead of the **My service group** view\. Everything else in the following procedure remains the same\.

In this case, we're adding Amazon EC2 using the Amazon EC2 **Quick estimate** option\. <a name="generate-quick-estimate"></a>

**To add and configure a service for your estimate**

1. On the **My service group** page choose **Add service**, which brings you to a page of services that you can add to your estimate\.

1. On the **Add service** page, select **Amazon EC2** and choose **Configure** in the upper\-right header\. This adds Amazon EC2 to your group and takes you to the **Quick estimate** view, where you can configure what you want in an Amazon EC2 instance\.

   The **Quick estimate** view is preloaded with default values, enabling you to see a starting estimate without adding or changing any information\. You can change any of the values for the following parameters or keep the defaults:
   + The operating system
   + The number of Amazon EC2 instances
   + The Amazon EC2 instance search options
   + The pricing model
   + The reservation term
   + The payment options
   + The storage volume
   + The storage amount

1. Choose **Add to my estimate**\.

   This adds an Amazon EC2 instance with the selected parameters to the group that you created in step one and returns you to the **My estimate** page\. 

   The **My service group** page shows you how much the selected default instance would likely cost you\. Note that estimates are just that: estimates\. AWS charges are calculated using the actual AWS usage for an account\.