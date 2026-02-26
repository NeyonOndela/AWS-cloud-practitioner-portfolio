## Creating Networking Resources in an Amazon Virtual Private Cloud (VPC)


## Introduction
In this lab, I was tasked with designing and configuring a fully functional and routable network within an Amazon Virtual Private Cloud (VPC). The primary objective was to create and configure the necessary AWS networking components including a VPC, Internet Gateway, Route Table, Security Group, Network Access Control List (NACL), and an EC2 instance so that the instance could successfully communicate with external networks using the ping command.The lab was considered complete once I was able to successfully ping an external IP address from within the EC2 instance.


## Objectives
- Create a custom VPC

- Configure a Subnet

- Create and attach an Internet Gateway

- Configure a Route Table

- Create and configure a Security Group

- Configure a Network Access Control List (NACL)

- Launch an EC2 instance inside the VPC

- Verify external connectivity





## Scenario
Your role is a Cloud Support Engineer at Amazon Web Services (AWS). During your shift, a customer from a startup company requests assistance regarding a networking issue within their AWS infrastructure. The email and an attachment of their architecture is below.

## Email from the customer
"Hello Cloud Support!
I previously reached out to you regarding help setting up my VPC. I thought I knew how to attach all the resources to make an internet connection, but I cannot even ping outside the VPC. All I need to do is ping! Can you please help me set up my VPC to where it has network connectivity and can ping? The architecture is below. Thanks!

Brock, startup owner"


<img width ="1000" height="500" alt="instance1" src= "https://github.com/NeyonOndela/AWS-cloud-practitioner-portfolio/blob/f74b1e42e962114d25e9835e5cf877e69705085d/Resources/customer%20arch.jpg" />


## Creating a Subnet

Next, I created a public subnet within the VPC. I ensured it was associated with the correct Availability Zone and CIDR range.
To make it public, I configured it to automatically assign public IPv4 addresses to instances launched within it.

<img width ="1000" height="500" alt="instance1" src= "https://github.com/NeyonOndela/AWS-cloud-practitioner-portfolio/blob/8847cfd0760291c575adc04b780e910210679c23/Resources/networkl.jpg" />

## Creating and Attaching an Internet Gateway

To enable internet access, I created an Internet Gateway and attached it to my VPC. Without this step, instances inside the VPC would not be able to communicate with external networks.

<img width ="1000" height="500" alt="instance1" src=""






 
