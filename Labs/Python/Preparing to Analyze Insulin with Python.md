## Preparing to Analyze Insulin with Python

## Overview

In this project, I worked with biological sequence data and prepared it for analysis using Python in the AWS Cloud9 development environment. The purpose of this lab was to retrieve the protein sequence of human insulin from the preproinsulin molecule and organize the data for further processing.

Human insulin is a hormone that regulates blood sugar levels in the body. In fields such as bioinformatics and scientific computing, Python is commonly used to manipulate and analyze biological sequences. In this lab, I retrieved the human preproinsulin sequence from the **National Center for Biotechnology Information (NCBI)** database and processed the raw data by cleaning the sequence and extracting the relevant amino acid segments.
This lab helped me understand how biological data can be structured and prepared before performing  analysis.

## Objectives

The aim of this lab was to be able to:
- Access and use the AWS Cloud9 integrated development environment

- Retrieve biological sequence data from NCBI

- Clean raw protein sequence data by removing unnecessary formatting

- Extract specific amino acid segments from the preproinsulin sequence

- Prepare the dataset for further analysis using Python


 ## Retrieving the Human Preproinsulin Sequence
 I retrieved the human preproinsulin sequence from the NCBI database
 <img width ="1000" height="500" alt="NCBI website" src="https://github.com/NeyonOndela/AWS-cloud-practitioner-portfolio/blob/42d01a846fb38cc2d2b696497a7599e2cac6c4d3/Labs/Python/analyze2.jpg"/>
Steps I followed:
- I opened the NCBI website.
-From the search dropdown, I selected Protein.
- I searched for human insulin.
- From the search results, I selected insulin [Homo sapiens].
- At the bottom of the record, I copied the protein sequence starting from ORIGIN and ending with //.
  
The sequence looked like this:
**ORIGIN
1 malwmrllpl lallalwgpd paaafvnqhl cgshlvealy lvcgergffy tpktrreaed
61 lqvgqvelgg gpgagslqpl alegslqkrg iveqcctsic slyqlenycn
//**
I then created a new file in Cloud9 called:
*preproinsulin-seq.txt*
I pasted the copied sequence into this file. This file contains the raw biological sequence data exactly as retrieved from NCBI.

## Cleaning the Sequence

The raw sequence contained characters that were not part of the amino acid sequence, such as:

- the word ORIGIN

- numbers 1 and 61

- spaces

- line breaks

- the // termination symbol

Using Python, I removed these characters to produce a continuous amino acid sequence.
I saved the cleaned sequence in a file called:
**preproinsulin-seq-clean.txt*


<img width ="1000" height="500" alt="Database file" src="https://github.com/NeyonOndela/AWS-cloud-practitioner-portfolio/blob/4c6e12b405ca8bd5aec8a83c9ca1d00979f5d684/Labs/Python/updated%201.jpg"/>
 

## Extracting Insulin Sequence Segments Using Python

To complete this part of the lab, I used **Python** to extract specific amino acid segments from the cleaned preproinsulin sequence. After cleaning the original sequence and saving it in `preproinsulin-seq-clean.txt`, the file contained **110 lowercase characters**, each representing an amino acid.

Using Python string manipulation and slicing, I separated the sequence into different sections based on the amino acid positions required in the lab instructions. Python made this process efficient because it allows easy extraction of specific parts of a sequence using index ranges.

First, I extracted **amino acids 1–24**, which represent the **signal peptide**. I used Python slicing to select the first 24 characters from the cleaned sequence and saved the result in a file named `lsinsulin-seq-clean.txt`. After saving the sequence, I verified that the file contained **24 characters**.

Next, I extracted **amino acids 25–54**, which correspond to the **B-chain of insulin**. Using Python slicing again, I selected the appropriate portion of the sequence and saved it in `binsulin-seq-clean.txt`. I confirmed that this file contained **30 characters**, which matches the expected length for this segment.

After that, I extracted the **C-peptide**, which corresponds to **amino acids 55–89**. This portion connects the A-chain and B-chain during insulin formation but is removed during the final processing of insulin. I used Python to extract this section and saved it in `cinsulin-seq-clean.txt`. I then verified that the file contained **35 characters**.

Finally, I extracted **amino acids 90–110**, which represent the **A-chain of insulin**. I used Python slicing to retrieve this segment and saved it in `ainsulin-seq-clean.txt`. I confirmed that this file contained **21 characters**, which is the correct length for the A-chain.

By using Python to perform these extractions, I was able to efficiently separate the different parts of the preproinsulin sequence and save them into individual files. This approach demonstrates how Python can simplify biological data processing tasks and prepare datasets for further analysis in bioinformatics workflows.

<img width ="1000" height="500" alt="Database file" src="https://github.com/NeyonOndela/AWS-cloud-practitioner-portfolio/blob/4c6e12b405ca8bd5aec8a83c9ca1d00979f5d684/Labs/Python/analyze6.jpg"/>
<img width ="1000" height="500" alt="Database file" src="https://github.com/NeyonOndela/AWS-cloud-practitioner-portfolio/blob/4c6e12b405ca8bd5aec8a83c9ca1d00979f5d684/Labs/Python/analyze7.jpg"/>

## Learning Outcome

Through this lab, I gained hands-on experience retrieving biological sequence data and preparing it for computational analysis. I also strengthened my understanding of how Python can be applied in bioinformatics and scientific computing to manipulate and analyze protein sequences efficiently.
This lab is part of my continuous learning journey in cloud computing , where I document hands-on labs and practical exercises as I build my technical skills.








