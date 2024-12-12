# Portfolio-Part-2
This project shows the details of my project part 2

In this project, I focused on implementing data quality control measures as part of the Data Analytics Platform (DAP) for the City of Vancouver. My objective was to ensure the accuracy, completeness, consistency, and security of data across various AWS services. This included encrypting sensitive data, validating datasets, and creating monitoring systems for data quality and availability.


**5. Data Enriching**

I organized and enriched raw data stored in AWS S3 buckets to prepare it for analysis. The goal was to handle structured, semi-structured, and unstructured data types seamlessly.

**Process**

I created a clickstream folder in the raw S3 bucket to segregate data logically.
Using AWS DynamoDB, I created a table, added sample items, and exported this data to the clickstream folder. This process introduced structured, semi-structured, and unstructured data types into the pipeline.

Next, I used AWS Glue to create a Data Catalog and configured a crawler to scan and organize data from all subfolders in the raw bucket. This ensured data was cataloged with appropriate schemas and made query-ready for AWS Athena.

**Deliverables**

A structured AWS Glue Data Catalog containing all tables.

Query-ready datasets accessible via Athena.

![image](https://github.com/user-attachments/assets/d8d618a9-3893-4a1e-8b2e-592d2389febd)


![image](https://github.com/user-attachments/assets/c3f3de3e-ebeb-444f-9912-b2226272f318)

![image](https://github.com/user-attachments/assets/8d08c703-ca00-4fa8-93f4-85440f9ad5e5)

![image](https://github.com/user-attachments/assets/e36283ac-de79-4411-9a9a-ea8b843f97c8)

**6. Data Protection**

**Objective**

My goal was to implement robust data protection mechanisms for the data stored in S3 buckets. This included encryption, versioning, and backup strategies to prevent unauthorized access and ensure data durability.

Process

**Encryption:**

I created a symmetric key using AWS KMS, which supports both encryption and decryption.

This key was applied to S3 buckets for default encryption, ensuring all uploaded objects were encrypted automatically.

**Versioning**:

I enabled versioning on all S3 buckets. This tracks every modification to stored objects, protecting data against accidental overwrites or deletions.

**Replication**:

Backup buckets were created in a different AWS region.

I configured replication rules to automatically sync data from primary buckets to backup buckets, ensuring high availability.

**Deliverables**

Encrypted and version-controlled S3 buckets.

Backup buckets with active cross-region replication rules.

![image](https://github.com/user-attachments/assets/f61e592a-ad5b-4c04-8277-4557da0b66e7)

![image](https://github.com/user-attachments/assets/9d78355f-2906-4388-a3c4-e0a045f513b6)

![image](https://github.com/user-attachments/assets/6d34af03-ec9c-455c-8261-f5896d0283c7)

**7. Data Governance**

Objective

To ensure the usability, security, and compliance of the data, I implemented data governance measures focusing on quality and sensitive information protection.

**Process**

I sourced clean data from AWS DataBrew, where preprocessing tasks were completed in earlier phases.

Using AWS Glue, I checked datasets for sensitive information (e.g., PII) and ensured compliance by masking or encrypting any identified fields.

I validated data quality by ensuring completeness and uniqueness using SQL queries.

**Pipeline Enhancements
**
I introduced aggregate blocks to calculate required metrics and applied conditional routing to organize data into destination folders based on specific criteria.

**Deliverables**

A governance-compliant dataset with sensitive information handled appropriately.

Organized data pipelines ready for downstream consumption.

![image](https://github.com/user-attachments/assets/4c458dbc-7f04-4e1b-9d60-766e5a5fd380)

![image](https://github.com/user-attachments/assets/1fcb4aa3-dbc6-4585-9754-1ae72e8f12e3)

**8. Data Observability**

**Objective**

To monitor the health of data pipelines and AWS resource usage, I set up observability measures using AWS CloudWatch.

**Process**

I created a CloudWatch dashboard to visualize:

Storage growth in S3 buckets.

Resource utilization metrics for AWS Glue and EC2.

Cost trends for AWS services.

The dashboard allowed me to track anomalies in data or resource usage, ensuring the smooth operation of the DAP.

**Deliverables**

A CloudWatch dashboard with metrics and alerts for monitoring resource performance and cost.

![image](https://github.com/user-attachments/assets/91f7037c-c7f9-49cd-973c-ad03e8aaf475)


By implementing data quality control measures, I ensured that the data pipeline for the DAP was secure, reliable, and compliant with best practices. These steps prepared the data for advanced analytics and demonstrated the scalability and robustness of AWS services. The combination of encryption, governance, and observability tools made the platform ready for high-quality analysis and operational success.
