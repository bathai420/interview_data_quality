# Data Governance
<!-- TOC -->
[HOME](https://github.com/bathai420/interview_data_quality/tree/main), 
[About](https://github.com/bathai420/interview_data_quality/blob/main/About/README.md),
[Interest](https://github.com/bathai420/interview_data_quality/blob/main/Interest/README.md), 
[DATA GOVERNANCE](https://github.com/bathai420/interview_data_quality/blob/main/DataGovernance/README.md)

Data governance refers to a set of policies, roles, and standards established in an organization to ensure the quality, security, accuracy, and usability of data throughout its lifecycle.

There are four pillars of data governance such as
1) data management:
   1) It ensures that the data is gathered, organized, and used appropriately to meet business needs.
   2) Using technics like
      1) Discovery: It is a process of understanding all different assets across organization, which may be from On-Prem or Cloud
      2) Classification: Is a technic to categorizing the data. Like customer data, product data, patient data, claims data etc..
      3) Example:
         1) Identify Patient/Member information across organization, define metadata for each element, and store centrally as a data catalog (data dictionary)
         2) Data governance defines who can see data, how can access, and when. Data management implements these policies with technical solutions to store, organize, and use the data.
2) data quality:
   1) It is a measure to check the condition of the data based on factors like timeliness, completeness, accuracy, and consistency
   2) Bad data quality impacts business and customer performance. It will lead into inaccurate insights, poor decision-making, waste of resources, and miss business opportunities.
   3) Example:
      1) In one of my project, Patient address and provider address has an important role to place patients in-care, by identify the nearby provider. We implemented data quality check on address attributes and communicated with insurance company to fix the issue and send clean data
3) data security:
   1) Data security protects data, decides who should have access to the data.
   2) Some information is extremely private (example: SSN, Address, Medical record number, Account number, Phone numbers, etc..) and need access to specific users. By having correct access controls inplace.
   3) Sensitive information must be masked, hashed, or encrypted form other users
4) compliance:
   1) Compliance is a process to define and follow rules, regulations, and standards relevant to their business processes.
   2) Examples:
      1) In health care HIPAA compliance was created to safeguard the data and privacy of their patient personal medical information.


[HOME](https://github.com/bathai420/interview_data_quality/tree/main), 
[About](https://github.com/bathai420/interview_data_quality/blob/main/About/README.md),
[Interest](https://github.com/bathai420/interview_data_quality/blob/main/Interest/README.md), 
[DATA GOVERNANCE](https://github.com/bathai420/interview_data_quality/blob/main/DataGovernance/README.md)