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



## Configuring the Route Table

I modified the VPC’s route table by adding a new route:
Destination: 0.0.0.0/0
Target: Internet Gateway
I then associated this route table with my public subnet. This ensured that outbound internet traffic would be properly routed.
<img width ="1000" height="500" alt="instance1" src="https://github.com/NeyonOndela/AWS-cloud-practitioner-portfolio/blob/a2c961a47d231173f12b26ecfbb90c4f0a14b9ed/Resources/netw.jpg" />

## Creating and Attaching an Internet Gateway

To enable internet access, I created an Internet Gateway and attached it to my VPC. Without this step, instances inside the VPC would not be able to communicate with external networks.

<img width ="1000" height="500" alt="instance1" src="https://github.com/NeyonOndela/AWS-cloud-practitioner-portfolio/blob/62375806e17ec9ad96516ec8f487d9cf3814deeb/Resources/internet%20geway.jpg" />




## Configuring the Network Access Control List (NACL)

I reviewed the default NACL settings and ensured that both inbound and outbound traffic allowed:
- ICMP
- SSH
- Ephemeral ports for return traffic
  
Unlike Security Groups, NACLs are stateless, meaning both inbound and outbound rules must be explicitly defined.


## Configuring the Security Group

I created a Security Group to act as a virtual firewall for my EC2 instance.

I configured:

- SSH (Port 22) for remote access

- ICMP for ping testing

- Allowed outbound traffic to all destinations

Security Groups are stateful, meaning return traffic is automatically allowed.


<img width ="1000" height="500" alt="instance1" src="https://github.com/NeyonOndela/AWS-cloud-practitioner-portfolio/blob/ae55a08b1f8e98edb85d95b90836c82c59bde4b7/Resources/net.jpg" />


## Launching the EC2 Instance

I launched an EC2 instance within the configured subnet and attached the Security Group created earlier.
I verified:
- The instance had a public IP address
- The subnet was associated with the correct route table
- The Internet Gateway was attached to the VPC


<img width ="1000" height="500" alt="instance1" src="https://github.com/NeyonOndela/AWS-cloud-practitioner-portfolio/blob/857401133cf6a7ef56178f6bc35f1b1a4f313ff3/Resources/net%20instance.jpg" />


 ## Using ping to test internet connectivity

<img width ="1000" height="500" alt="instance1" src= "" 






 
