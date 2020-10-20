# Create New stack for CloudFormation  

Sign in to the AWS Management Console and open the AWS CloudFormation console at https://console.aws.amazon.com/cloudformation.

If this is a new AWS CloudFormation account, click Create New Stack. Otherwise, click Create Stack.In the Template section, 
select upload from file and select *az.yaml from your directory.
In the Specify Details section, enter a stack name in the Name field. For this example, use MultiAZ-VPC.

## Easily Create VPC with CloudFormation Script
Here we have three scenario where i can create VPC in following ways.

1:-VPC with private and public subnets in two Availability Zones (2az.yaml)

2:-VPC with private and public subnets in three Availability Zones (3az.yaml)

3:-VPC with private and public subnets in Four Availability Zones (4az.yaml)

## Two Availability zone based VPC

![Screenshot](https://raw.githubusercontent.com/pratiknborkar/VPC-Templates/main/Images/2az.png)

## Three Availability zone based VPC

![Screenshot](https://raw.githubusercontent.com/pratiknborkar/VPC-Templates/main/Images/3az.png)

## Four Availability zone based VPC

![Screenshot](https://raw.githubusercontent.com/pratiknborkar/VPC-Templates/main/Images/4az.png)

## NAT Gateway
This script describes a NAT Gateway that forwards HTTP, HTTPS traffic from a single private subnet to the Internet. 
You need one stack per availability zone. 
Example: If you use the 2azs.yaml template, you will need two Nat Gateway stack in A and B.
You need one Gateway in each SubnetZone (e.g. A and B in 2azs.yaml).

![Screenshot](https://raw.githubusercontent.com/pratiknborkar/VPC-Templates/main/Images/vpc-nat-gateway%20.png)

## Clean up
To delete the stack From the AWS CloudFormation console, select the  MultiAZ-VPC stack.

Click Delete Stack.

In the confirmation message that appears, click Yes, Delete.

The status for  MultiAZ-VPC changes to DELETE_IN_PROGRESS. In the same way you monitored the creation of the stack, you can monitor its deletion by using the Event tab. When AWS CloudFormation completes the deletion of the stack, it removes the stack from the list.

## Note.
Following all there VPC script creates, Only subnets in multiple availability zone and routing table without Internet Gateway and Nat Gateway.

If you want to allow internet in Public subnets then you must attached internet gateway on Public Routing table.
If you want to allow internet in Private subnets then you must attached NAT gateway on Public Routing table.
 

