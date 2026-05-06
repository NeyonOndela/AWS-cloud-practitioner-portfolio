## Connecting VPCs
**Overview**

In this exercise, I explored and implemented VPC peering to enable secure, private communication between separate Virtual Private Clouds. Through this SimuLearn, I configured peering connections, updated routing at the subnet level, and developed a deeper understanding of how multi-VPC architectures can communicate without routing traffic over the public internet.

**Services I Worked With**
* Amazon VPC (Virtual Private Cloud) — Created isolated network environments with customizable subnets, route tables, and networking configurations
* Amazon Elastic Compute Cloud (EC2) — Launched instances in different VPCs to test and validate connectivity across peered networks


**Through this SimuLearn exercise, I demonstrated the ability to:**

* Understand how VPC peering enables private, low-latency communication between VPCs without relying on internet gateways
* Plan and execute the steps required to establish peering connections, including request creation, acceptance, and route table updates
* Configure active peering connections and ensure bidirectional communication between VPCs
* Implement routing rules at the subnet level using destination CIDR blocks to direct traffic through peering links
* Recognize key limitations of VPC peering, such as non-transitive connectivity and the need for non-overlapping IP ranges
* Validate connectivity by testing communication between EC2 instances across different VPCs

<img width ="800" height="400" alt="aws cloud certificate" src="https://github.com/NeyonOndela/AWS-cloud-practitioner-portfolio/blob/a409d40d4b05d06685bac6d3fe54f101483aa8e6/Resources/aws%20vpc%20peering.jpg" />
<img width ="800" height="400" alt="aws cloud certificate" src="https://github.com/NeyonOndela/AWS-cloud-practitioner-portfolio/blob/a409d40d4b05d06685bac6d3fe54f101483aa8e6/Resources/ConnectingVPCs.png" />
