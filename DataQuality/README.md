# DATA QUALITY

<!-- TOC -->
[About](https://github.com/bathai420/interview_data_quality/blob/main/About/README.md),
[Interest](https://github.com/bathai420/interview_data_quality/blob/main/Interest/README.md),
[AMBIGUITY](https://github.com/bathai420/interview_data_quality/blob/main/Ambiguity/README.md),
[DATA GOVERNANCE](https://github.com/bathai420/interview_data_quality/blob/main/DataGovernance/README.md),
[Data Quality](https://github.com/bathai420/interview_data_quality/blob/main/DataQuality/README.md), 
[FRAUD DATA](https://github.com/bathai420/interview_data_quality/blob/main/FraudData/README.md),
[Work Environment](https://github.com/bathai420/interview_data_quality/blob/main/WorkEnvironment/README.md),
[New Skill](https://github.com/bathai420/interview_data_quality/blob/main/NewSkill/README.md),
[Cross-Functional](https://github.com/bathai420/interview_data_quality/blob/main/CrossFunctional/README.md),
[Issues](https://github.com/bathai420/interview_data_quality/blob/main/Issues/README.md),
[Projects](https://github.com/bathai420/interview_data_quality/blob/main/Projects/README.md),
[Questions](https://github.com/bathai420/interview_data_quality/blob/main/Questions/README.md),
[Mistake](https://github.com/bathai420/interview_data_quality/blob/main/Mistake/README.md)

Data Quality measures how well a data set perform checks for
 
1) Timeliness
2) Completeness
3) Accuracy
4) Consistency
5) Uniqueness
6) Validity checks

**_Timeliness:_**

In a business environment, it is essential that data is transferred from the source to the target system in a timely manner to support up-to-date decision-making. As part of data quality checks, the goal is to verify that data is delivered within the expected timeframe to ensure timeliness. I perform timestamp or filename comparisons to validate this. For example, files may include a datetime in the filename, which we use to check the target system. In the database, I compare the maximum datetime from the source and compare it with the target.

**_Accuracy:_**

In a business environment, it is essential that data is accurate and correctly reflects the real-world information it represents. As part of data quality checks, the goal is to verify that the data in the target system matches the source data. For example, I might compare customer addresses in the source database with those in the customers table (customer relationship management system) to identify any inconsistency.

**_Completeness:_**

In a data-driven environment, it is crucial to ensure that all required data is fully transformed from the source to the target system. As part of data quality checks, the goal is to verify that no data is missing between the source and target systems. To ensure completeness, I perform row count comparisons between the source and target using tools like Python for file systems and SQL for databases to verify that no data is missing.

**_Uniqueness:_**

In a data system, each entity should be recorded only once without duplication. The goal is to ensure that each record in a dataset is unique. To verify uniqueness, I perform checks using SQL queries that identify duplicate records.

**_Consistency:_**

In a data environment, data can be stored in multiple locations, systems, or formats. As part of a data quality check, the goal is to ensure that the data is consistent across all systems. This means that values stored in different databases or files should match, and the data format and structure should be the same. We perform hash column consistency checks by creating a hash for each row on both the source and target using the SHA-5 function in SQL.

**_Validity checks:_**

Validity checks will check like

1) SSN column, can not have any nulls

2) Zip Code column, Zip code should be of length 5 characters

example for dq

In one of my project, Patient address and provider address has an important role to place patients in-care. In order to place a patient in-care we need to identify the nearby provider who is close to the patient address/location.

Analyse the target data using sql to check weather there are any nulls for the address column if i find any null values i document the percentage of null values for the target table and i also check the source table if it is a csv file i use python code using data frame to check the percentage of null.

[About](https://github.com/bathai420/interview_data_quality/blob/main/About/README.md),
[Interest](https://github.com/bathai420/interview_data_quality/blob/main/Interest/README.md),
[AMBIGUITY](https://github.com/bathai420/interview_data_quality/blob/main/Ambiguity/README.md),
[DATA GOVERNANCE](https://github.com/bathai420/interview_data_quality/blob/main/DataGovernance/README.md),
[Data Quality](https://github.com/bathai420/interview_data_quality/blob/main/DataQuality/README.md), 
[FRAUD DATA](https://github.com/bathai420/interview_data_quality/blob/main/FraudData/README.md),
[Work Environment](https://github.com/bathai420/interview_data_quality/blob/main/WorkEnvironment/README.md),
[New Skill](https://github.com/bathai420/interview_data_quality/blob/main/NewSkill/README.md),
[Cross-Functional](https://github.com/bathai420/interview_data_quality/blob/main/CrossFunctional/README.md),
[Issues](https://github.com/bathai420/interview_data_quality/blob/main/Issues/README.md),
[Projects](https://github.com/bathai420/interview_data_quality/blob/main/Projects/README.md),
[Questions](https://github.com/bathai420/interview_data_quality/blob/main/Questions/README.md),
[Mistake](https://github.com/bathai420/interview_data_quality/blob/main/Mistake/README.md),
[Conflict](https://github.com/bathai420/interview_data_quality/blob/main/Conflict/README.md)