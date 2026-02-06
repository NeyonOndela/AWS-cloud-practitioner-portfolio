# AWS EC2 LAB 


## Overview

This lab provided practical experience with Amazon EC2, covering instance deployment, configuration, security, monitoring, and scaling. It also included deploying a web server and exploring automation and lifecycle management in a real-world cloud environment.

---

1. I began by logging into the AWS Management Console, then selected Instances from the left navigation pane and created an EC2 instance named **Web Server**. for **Amazon machine image(AMI)** i used **Amazon linux 2023 AMI** and i chose  t3.micro instance type, enabling protection to safeguard the instance from accidental removal. I also applied a **user Data script** to automatically install the **Apache web server** and set up a basic web page during launch.
<img width ="1000" height="500" alt="instance1" src= "https://github.com/NeyonOndela/zomato-project-2023/blob/63395a954c26bee0832969ddeea9e7b3e457a822/instance1.jpg " />
<img width ="1000" height="500" alt="instance2" src="https://github.com/NeyonOndela/zomato-project-2023/blob/63395a954c26bee0832969ddeea9e7b3e457a822/instance3.jpg" />
<img width ="1000" height="500" alt="instance4" src="https://github.com/NeyonOndela/zomato-project-2023/blob/63395a954c26bee0832969ddeea9e7b3e457a822/instance5.jpg" />
<img width="1000" height="500" alt ="instance8" src="https://github.com/NeyonOndela/zomato-project-2023/blob/63395a954c26bee0832969ddeea9e7b3e457a822/instance8.jpg" />
<img width="1000" height ="500" alt="instance10" src="https://github.com/NeyonOndela/zomato-project-2023/blob/63395a954c26bee0832969ddeea9e7b3e457a822/instance10.jpg" />

---

## The instance was launched suceessfully

<img width="1000" height="500" alt ="instance11" src="https://github.com/NeyonOndela/zomato-project-2023/blob/63395a954c26bee0832969ddeea9e7b3e457a822/instance11.jpg" />

---
## Monitoring the instance

After the instance was up and running, I reviewed the available monitoring features. I verified both system and instance health using **Status Checks**, analyzed **CloudWatch metrics** to gain performance insights, and took an instance screenshot to simulate console-level access.

 <img width="1000" height="500" alt="instance12" src="https://github.com/NeyonOndela/zomato-project-2023/blob/63395a954c26bee0832969ddeea9e7b3e457a822/instance12.jpg" />
<img width ="1000" height="500" alt="instance13" src= "https://github.com/NeyonOndela/zomato-project-2023/blob/63395a954c26bee0832969ddeea9e7b3e457a822/instance13.jpg" />

----
## The security group was updated to allow the required inbound traffic, and the web server was accessed successfully through a web browser.

<img width="1000" height="500" alt="instance14" src="https://github.com/NeyonOndela/zomato-project-2023/blob/63395a954c26bee0832969ddeea9e7b3e457a822/instance14.jpg" />

---

## The instance was resized by modifying the instance type and adjusting the EBS volume to meet the required performance and storage needs.

**How did i accomplish this?** I stopped the EC2 instance and resized it from t3.micro to t3.small, which increased the available memory. I then modified the root EBS volume, expanding it from 8 GiB to 10 GiB, and restarted the instance. This task demonstrated how EC2 resources can be adjusted dynamically to meet changing workload requirements during operation.

<img width ="1000" height="500" alt="instance13" src="https://github.com/NeyonOndela/zomato-project-2023/blob/63395a954c26bee0832969ddeea9e7b3e457a822/instance15.jpg" />

<img width ="1000" height="500" alt="instance16" src="https://github.com/NeyonOndela/zomato-project-2023/blob/63395a954c26bee0832969ddeea9e7b3e457a822/instance16.jpg" />
<img width ="1000" height="500" alt="instance16" src="https://github.com/NeyonOndela/zomato-project-2023/blob/63395a954c26bee0832969ddeea9e7b3e457a822/instance17.jpg" />
<img width ="1000" height="500" alt="instance16" src="https://github.com/NeyonOndela/zomato-project-2023/blob/63395a954c26bee0832969ddeea9e7b3e457a822/instance18.jpg" />



----
## Test Termination Protection

I tested termination protection by attempting to delete the instance while the protection was enabled, which prevented the action. After disabling termination protection, I was able to successfully terminate the instance. This exercise demonstrated the role of safeguards in preventing accidental deletion of resources in production environments.

<img width="1000" height="500" alt="instance19" src="https://github.com/NeyonOndela/zomato-project-2023/blob/63395a954c26bee0832969ddeea9e7b3e457a822/instance19.jpg" />











