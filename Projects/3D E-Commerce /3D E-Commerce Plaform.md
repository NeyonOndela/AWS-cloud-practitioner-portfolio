<img width="597" height="857" alt="image" src= "https://github.com/NeyonOndela/AWS-cloud-practitioner-portfolio/blob/b5658ddf501fe4a07a399a66ab59946a99f20281/Resources/3sa.jpg" />


## 3D E-Commerce Platform Architecture Overview

The proposed AWS architecture is designed to provide a secure, scalable, and highly available platform for a 3D web application. User requests are first routed through Amazon Route 53, which directs traffic to Amazon CloudFront. CloudFront serves as a content delivery network (CDN), ensuring fast delivery of content to users worldwide. Static 3D assets are delivered directly from Amazon S3, while dynamic requests are routed to an Application Load Balancer (ALB) that distributes traffic across EC2 instances deployed in multiple Availability Zones.

The application's backend is hosted on Amazon EC2 instances with Amazon EBS volumes attached to provide persistent storage. AWS Lambda is used to perform serverless background tasks, including 3D asset processing and generating multiple levels of detail. For data management, Amazon DynamoDB stores metadata and session information requiring low-latency access, while Amazon Aurora (RDS), configured across multiple Availability Zones, manages transactional data such as customer records and orders. Amazon ElastiCache (Redis) improves performance by caching frequently accessed scene data, reducing the load on the databases.

Application monitoring, performance tracking, and cost optimization are supported through Amazon CloudWatch and AWS Trusted Advisor, helping maintain system health and operational efficiency.

## Why Each AWS Service Was Chosen

* **Amazon Route 53** manages DNS routing and performs health checks to ensure users are directed to healthy and available application resources.

* **Amazon CloudFront** delivers and caches large 3D assets at edge locations closer to users, reducing latency, improving load times, and minimizing requests to the backend infrastructure.

* **Amazon S3** serves as the storage solution for 3D models, textures, thumbnails, and pre-generated levels of detail (LODs). It offers highly durable, scalable, and cost-efficient storage, while lifecycle policies help optimize long-term storage costs.

* **Application Load Balancer (ALB)** evenly distributes incoming application traffic across EC2 instances deployed in multiple Availability Zones, increasing both application availability and fault tolerance.

* **Amazon EC2**, supported by **Amazon EBS**, hosts the backend application. EC2 provides scalable compute capacity, while EBS delivers persistent block storage. Spot Instances can also be used for non-essential workloads to reduce operational costs.

* **AWS Lambda** handles serverless, event-driven tasks such as generating thumbnails and processing or converting 3D assets automatically.

* **Amazon DynamoDB** is selected for workloads that require low-latency access and seamless scalability, making it ideal for managing session information, product catalogs, and other frequently accessed data.

* **Amazon Aurora (Amazon RDS)** stores transactional information, including customer orders and payment records. Deploying Aurora in a Multi-AZ configuration enhances database availability and resilience.

* **Amazon ElastiCache (Redis)** improves application performance by caching frequently requested scene metadata in memory, reducing database load and accelerating response times.

* **Amazon CloudWatch** continuously monitors application and infrastructure performance, while **AWS Trusted Advisor** provides best-practice recommendations to optimize costs, security, reliability, performance, and service limits.


## How the Architecture Meets the Five Requirements?

### 1. High Availability

The architecture is built to maintain service availability even if individual components experience failures. Key services such as the Application Load Balancer (ALB), Amazon EC2 instances, Amazon Aurora, and Amazon ElastiCache are deployed across multiple Availability Zones to improve fault tolerance. Amazon Route 53 health checks automatically redirect traffic away from unhealthy resources, while Amazon CloudFront and Amazon S3 ensure reliable delivery of static content.

### 2. Scalability

The solution is designed to handle changing workloads efficiently. Amazon EC2 Auto Scaling automatically increases or decreases the number of EC2 instances based on demand. Amazon DynamoDB seamlessly scales to accommodate traffic fluctuations, AWS Lambda automatically scales event-driven workloads, and Amazon CloudFront reduces backend load by serving cached content from edge locations.

### 3. Performance

Application performance is enhanced through Amazon CloudFront, which delivers content from locations closer to users, reducing latency. Amazon ElastiCache (Redis) provides fast in-memory caching for frequently accessed data, while compressed 3D assets and pre-generated Levels of Detail (LODs) reduce file sizes, resulting in faster loading and smoother rendering.

### 4. Security

The architecture follows AWS security best practices by using IAM roles and policies that grant only the minimum permissions required. Sensitive data is protected through encryption both in transit and at rest, and all core resources are deployed within a secure Amazon VPC to minimize external exposure and strengthen network security.

### 5. Cost Optimization

The solution incorporates several cost-saving strategies to improve efficiency. Amazon S3 lifecycle policies automatically transition or remove older data to reduce storage costs. AWS Lambda is used for intermittent workloads, eliminating the need to provision dedicated servers, while EC2 Spot Instances lower compute costs for non-critical tasks. Additionally, Amazon CloudWatch and AWS Trusted Advisor provide monitoring and recommendations to help identify opportunities for cost optimization and eliminate unnecessary expenses.





## Conclusion

This architecture combines AWS managed services, Amazon EC2, and serverless technologies to deliver a solution that is highly available, scalable, secure, high-performing, and cost-effective. It is well suited for hosting a global 3D web application and can be easily expanded or adapted as user demand and business requirements evolve over time.






