## Creating Networking Resources in an Amazon Virtual Private Cloud (VPC)


## Introduction
In this lab, I was tasked with designing and configuring a fully functional and routable network within an Amazon Virtual Private Cloud (VPC). The primary objective was to create and configure the necessary AWS networking components including a VPC, Internet Gateway, Route Table, Security Group, Network Access Control List (NACL), and an EC2 instance so that the instance could successfully communicate with external networks using the ping command.The lab was considered complete once I was able to successfully ping an external IP address from within the EC2 instance.


## Objectives

- Create a custom VPC

- Configure an Internet Gateway for internet connectivity

- Set up a Route Table with appropriate routing rules

- Configure a Security Group to allow necessary inbound and outbound traffic

- Modify Network Access Control Lists (NACLs)

- Launch and configure an EC2 instance

- Successfully ping an external address outside the VPC

- Gain familiarity with the AWS Management Console



## Scenario
Your role is a Cloud Support Engineer at Amazon Web Services (AWS). During your shift, a customer from a startup company requests assistance regarding a networking issue within their AWS infrastructure. The email and an attachment of their architecture is below.

## Email from the customer
"Hello Cloud Support!
I previously reached out to you regarding help setting up my VPC. I thought I knew how to attach all the resources to make an internet connection, but I cannot even ping outside the VPC. All I need to do is ping! Can you please help me set up my VPC to where it has network connectivity and can ping? The architecture is below. Thanks!

Brock, startup owner"


<img width ="1000" height="500" alt="instance1" src= "https://github.com/NeyonOndela/AWS-cloud-practitioner-portfolio/blob/f74b1e42e962114d25e9835e5cf877e69705085d/Resources/customer%20arch.jpg" />
 
