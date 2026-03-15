## Freshly_Ground Café

Freshly_Ground is a fictional local café that I used as a case study to demonstrate how a small business can migrate from traditional on-premises systems to the cloud. The café is imagined as a cozy place loved by both coffee enthusiasts and book lovers—a space that blends the calmness of nature with the joy of reading.

In this project scenario, the café relied on outdated on-premises systems with very limited digital infrastructure. These systems caused operational challenges such as slow processes, occasional shutdowns, and poor online visibility. Because of these limitations, customer engagement was low and the café lacked a reliable solution for data backup and recovery.

In today’s digital environment, these issues made it difficult for the business to grow and compete with other cafés that already had modern online platforms. As part of my cloud learning journey, I designed a solution that migrates the café’s infrastructure to the cloud using **Amazon Web Services (AWS)**.

---

# Goals of the Migration

In this project, my goal was to migrate the café’s IT infrastructure to AWS in order to:

* Improve operational efficiency
* Strengthen customer engagement through a better online presence
* Modernize IT systems while improving security
* Enable flexible scalability as the business grows
* Reduce long-term operational costs
* Ensure high availability and reliable disaster recovery
* Support future innovation and digital expansion

---

# Proposed Solution: Migration to AWS Cloud Infrastructure

## 1. Cloud Infrastructure Migration

To solve the café’s challenges, I designed a cloud-based solution where the existing on-premises infrastructure is migrated to AWS. This migration allows the business to benefit from reliable cloud services, improved system availability, and easier management of digital resources.

---

## 2. Enhancing the Café’s Online Presence

Another important part of the solution was creating a website that allows the café to establish an online presence.

I developed and hosted a **static website** using **Amazon S3**, which allows the café to:

* Display the café’s menu and prices
* Share the café’s story and brand identity
* Provide contact and location information
* Improve brand visibility and reach more customers
* Create a foundation for future features such as online ordering or e-commerce

---

# Architecture

The architecture I designed shows how the café can use AWS services to host its website and support its digital infrastructure.

<img width="1000" height="500" alt="screenshot" src="https://github.com/NeyonOndela/AWS-cloud-practitioner-portfolio/blob/ea175b73f5dfa06dff45457e27e87d739f35be2f/Projects/Resources/Screenshot_20260207-004554~2.png" />

---

# Static Website Hosted on Amazon S3

As part of this project, I built and hosted a static website for **FreshlyGround Café** using Amazon S3.

The website showcases the café’s brand, menu, and atmosphere.

<img width ="1000" height="500" alt="screenshot" src="https://github.com/NeyonOndela/AWS-cloud-practitioner-portfolio/blob/ba6700b3e23e7db567046141aef9f897a3eeb331/Projects/Resources/IMG-20260205-WA0006.jpg" />

<img width ="1000" height="500" alt="screenshot" src="https://github.com/NeyonOndela/AWS-cloud-practitioner-portfolio/blob/c042d1836efd075c9a92bc718012d3a32114a7f4/Projects/Resources/IMG-20260205-WA0009.jpg" />

---

# Uploading Website Files

After creating the website files, I uploaded them to an S3 bucket to host the site.

<img width="1000" height="500" alt="screenshot" src="https://github.com/NeyonOndela/AWS-cloud-practitioner-portfolio/blob/53c839d4a4fc89e3f86a3590247d249baf8d04f8/Projects/Resources/545632552-8021f948-3795-4492-84a2-2dbbd1505653.jpg"/>

---

# Deploying the S3 Website

To deploy the website, I completed the following steps:

1. I created an S3 bucket named **freshlyground-cafe-website**
2. I enabled **Static Website Hosting** in the bucket settings
3. I uploaded all the website files from my project folder
4. I configured a **bucket policy** to allow public read access
5. I accessed the website through the **S3 website endpoint**

After completing these steps, the website was successfully deployed and accessible online.

<img width ="1000" height="500" alt="website" src="https://github.com/NeyonOndela/AWS-cloud-practitioner-portfolio/blob/29775ee28ea6f0da76acf111a510085769e7b6aa/Projects/Resources/545637222-6e485e88-4cfc-457f-9123-0085b209ac29~2.png"/>

You can access the deployed website using the link below:

[https://s3.eu-north-1.amazonaws.com/freshlyground.cafe-static-sitee/index.html](https://s3.eu-north-1.amazonaws.com/freshlyground.cafe-static-sitee/index.html)

---

# Learning Outcomes

Through this project, I developed and practiced several important cloud computing skills, including:

* Designing cloud architecture solutions
* Integrating AWS services
* Planning and simulating a cloud migration strategy
* Transitioning from on-premises systems to cloud infrastructure
* Applying cloud security best practices
* Understanding scalability and capacity planning
* Designing business-focused cloud solutions
* Deploying real-world cloud projects
* Hosting static websites using Amazon S3
* Considering cost optimization when building cloud solutions

---

# Conclusion: Transformation Achieved

This project demonstrates how cloud adoption can transform a small business. By migrating FreshlyGround Café’s infrastructure to AWS, I showed how the business could benefit from modern cloud technologies.

Through this transformation, the café gains:

* **Agility** – the ability to quickly introduce new digital features
* **Efficiency** – reduced IT complexity and maintenance
* **Innovation** – opportunities to experiment with new customer experiences
* **Resilience** – improved system reliability and disaster recovery
* **Growth** – the ability to scale operations as the business expands

---

# Note

This project is **fictional** and was created purely for **learning and academic purposes**. No real café operations, customer data, or sensitive information were used in the development of this project.


