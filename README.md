# Understanding Student Course Completion Patterns in Academic Programs

*A descriptive-analytics project deployed on AWS*

## Table of Contents

1. [Project Overview](#project-overview)
2. [Objectives](#objectives)
3. [Dataset](#dataset)
4. [Methodology](#methodology)
5. [Descriptive Statistics & Key Findings](#descriptive-statistics--key-findings)
6. [Tools & Technologies](#tools--technologies)
7. [AWS Architecture](#aws-architecture)

   * Deployment & Service Models
   * Cost Analysis
   * Global Infrastructure
   * Core AWS Services (IAM | VPC | Lambda | EBS)
8. [Deliverables](#deliverables)
9. [Repository](#repository)
10. [How to Re-run the Analysis](#how-to-re-run-the-analysis)
11. [References](#references)

---

## Project Overview

This project investigates how students progress through their courses—whether they *complete*, are *in progress*, or *do not complete*—to surface patterns that can help institutions improve academic support and curriculum design .

## Objectives

* Quantify completion, in-progress, and non-completion rates for each course.
* Detect temporal trends (e.g., months with higher completion).
* Identify courses with unusually high success or dropout rates.
* Provide actionable recommendations for instructors and administrators .

## Dataset

* **Size:** 50 student-course records
* **Fields:** `record_id`, `student_id`, `course_id`, `status` (Completed | In Progress | Not Completed), `raw_date`
* Dates were stored in a numeric serial format and converted to standard dates for analysis .

![image](https://github.com/user-attachments/assets/218fe56b-7dd2-4fd5-8ece-0d1acce2cd6a)


## Methodology

1. **Data Ingestion** – Loaded CSV and JSON files into an AWS-based Python environment.
2. **Data Cleaning** –

   * Converted numeric dates to `YYYY-MM-DD`.
   * Removed duplicates and corrected invalid values.
3. **Feature Engineering** – Derived monthly/annual completion aggregates and course-level groupings.
4. **Descriptive Analytics** – Produced counts, percentages, and visualizations (line, bar, pie, heat-map) to reveal patterns .

## Descriptive Statistics & Key Findings

![image](https://github.com/user-attachments/assets/54af11c4-849d-4899-a0ae-aa6a15690cda)


* Majority of students remain **In Progress**, indicating longer completion times.
* Courses **C005** and **C001** exhibit the highest completion rates, while **C006** and **C003** show elevated non-completion .
* Completion rates fluctuate throughout the year; certain months consistently peak, suggesting academic-calendar effects .
* Recommendation: focus intervention resources on low-performing courses and align support services with busy months .

![image](https://github.com/user-attachments/assets/58accaa4-a2af-4823-9f11-315dc8ca8665)

![image](https://github.com/user-attachments/assets/c207742d-cbda-4edb-a400-f3ee937aee8d)

![image](https://github.com/user-attachments/assets/1d5e3f36-c86b-447e-ba87-c6e3b4c891fb)


## Tools & Technologies

| Layer                     | Technology                             | Purpose                                          |
| ------------------------- | -------------------------------------- | ------------------------------------------------ |
| Data wrangling & analysis | **Pandas**, **NumPy**                  | Cleaning, aggregation                            |
| Visualization             | **Matplotlib**, **Seaborn** (optional) | Charts (line, bar, pie, heat-map)                |
| Platform                  | **AWS** (S3, IAM, Lambda, VPC, EBS)    | Scalable storage, compute, security, networking  |
| Prototyping               | **Excel**                              | Initial data auditing                            |

## AWS Architecture

### Deployment & Service Models

* **Traditional vs Cloud** deployment comparison illustrates AWS elasticity and reduced operational overhead.
* Cloud service layers: **IaaS → PaaS → SaaS**, each shifting responsibility from customer to provider .

![image](https://github.com/user-attachments/assets/413a930a-2068-4bce-b556-71f37160789a)

![image](https://github.com/user-attachments/assets/01b08f94-4e84-464b-8b35-cc7fa36940c7)

![image](https://github.com/user-attachments/assets/e31a4849-1ff0-41b0-8e99-4c4be3c0c11f)

![image](https://github.com/user-attachments/assets/199c7352-d54e-4977-81d4-01516110a57d)


### Cost Analysis

* Pay-as-you-go pricing, Reserved Instances, and tiered usage are evaluated with the **AWS Pricing Calculator** and TCO comparisons.
* Cost-management dashboards, forecasting, and AWS Organizations controls are highlighted .

![image](https://github.com/user-attachments/assets/c74e2e53-072b-476e-9383-4b5965f2d136)


### Global Infrastructure

AWS Regions and Availability Zones ensure low-latency access and high availability for worldwide users .

![image](https://github.com/user-attachments/assets/5db7af35-1fce-4a12-888d-cdfc3d1be1a1)


### Core AWS Services

| Service    | Role in Project                                                 |
| ---------- | --------------------------------------------------------------- |
| **IAM**    | Fine-grained user permissions for data access                   |
| **VPC**    | Isolated network controlling inbound/outbound traffic           |
| **Lambda** | Serverless execution of ETL jobs and scheduled analytics        |
| **EBS**    | Persistent block storage for datasets and intermediate results  |

![image](https://github.com/user-attachments/assets/14b283eb-a017-475f-80eb-c05eba716c07)

![image](https://github.com/user-attachments/assets/9399090a-f6ef-49a0-b940-6bf20c53f42a)

![image](https://github.com/user-attachments/assets/bd956131-3503-4d67-9159-f737cb7bc07e)


![image](https://github.com/user-attachments/assets/d7b16976-0461-4110-bb59-b720f90e3856)


## Repository

> **GitHub:** [https://github.com/salmasamihaws/aws](https://github.com/salmasamihaws/aws)&#x20;
