---
layout: post
title: "Blog 1"
---

AWS EC2 Instances
-----------------

An instance is a virtual server in the AWS cloud. With Amazon EC2, you can set up and configure the operating system and applications that run on your instance.

Amazon Elastic Block Store (EBS) is an easy to use, high performance block storage service designed for use with EC2s for both throughput and transaction intensive workloads at any scale.



The basic steps to launch an instance are as followed

1.      Open the Amazon EC2 console at https://console.aws.amazon.com/ec2/.

2.      From the console dashboard, choose Launch Instance.

3.      The Choose an Amazon Machine Image (AMI) page displays a list of basic configurations, called Amazon Machine Images (AMIs), that serve as templates for your instance. Select an HVM version of Amazon Linux 2. Notice that these AMIs are marked "Free tier eligible."

4.      On the Choose an Instance Type page, you can select the hardware configuration of your instance. Select the t2.micro type, which is selected by default. Notice that this instance type is eligible for the free tier.

5.      Choose Review and Launch to let the wizard complete the other configuration settings for you.

6.      On the Review Instance Launch page, under Security Groups, you'll see that the wizard created and selected a security group for you. You can use this security group, or alternatively you can select the security group that you created when getting set up using the following steps:

a.       Choose Edit security groups.

b.      On the Configure Security Group page, ensure that Select an existing security group is selected.

c.       Select your security group from the list of existing security groups, and then choose Review and Launch.

7.      On the Review Instance Launch page, choose Launch.

8.      When prompted for a key pair, select Choose an existing key pair, then select the key pair that you created when getting set up.

Alternatively, you can create a new key pair. Select Create a new key pair, enter a name for the key pair, and then choose Download Key Pair. This is the only chance for you to save the private key file, so be sure to download it. Save the private key file in a safe place. You'll need to provide the name of your key pair when you launch an instance and the corresponding private key each time you connect to the instance.

Warning

Don't select the Proceed without a key pair option. If you launch your instance without a key pair, then you can't connect to it.

When you are ready, select the acknowledgment check box, and then choose Launch Instances.

9.      A confirmation page lets you know that your instance is launching. Choose View Instances to close the confirmation page and return to the console.

10.  On the Instances screen, you can view the status of the launch. It takes a short time for an instance to launch. When you launch an instance, its initial state is pending. After the instance starts, its state changes to running and it receives a public DNS name. (If the Public DNS (IPv4) column is hidden, choose Show/Hide Columns (the gear-shaped icon) in the top right corner of the page and then select Public DNS (IPv4).)

11.  It can take a few minutes for the instance to be ready so that you can connect to it. Check that your instance has passed its status checks; you can view this information in the Status Checks column



You can't connect the instance unless it's launched with the key pair.

Make sure the instance gets terminated when done using:

1.      In the navigation pane, choose Instances. In the list of instances, select the instance.

2.      Choose Actions, Instance State, Terminate.

3.      Choose Yes, Terminate when prompted for confirmation.

Amazon EC2 shuts down and terminates your instance. After your instance is terminated, it remains visible on the console for a short while, and then the entry is deleted.
