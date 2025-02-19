# Issues or challenges

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
[Questions](https://github.com/bathai420/interview_data_quality/blob/main/Questions/README.md)

I acknowledge the challenges
1) I recognize that challenges are expected in any role
2) I have an ability to stay calm in the situation.
 
I consider all options to deal the challenge and discuss tem with my lead and client and more forward to handle the challenge.

One of the issue or challenge I can share is, In one of the client project, they were migrating the data from on-prem to cloud. We were asked to validate/compare the data is migrated properly. We had a callenge to compare large datasets between source and target (due to not having enough compute and long-running jobs), in this situation we took an iterative approach to validate data in smaller chunks

Optional:
The comparison is done by creating row hash value on both source and target, which is used to compare the records like A-B and B-A 

SQL:

select * from source_table

except

select * from target_table;

(or)

select row_hash from source_table

except

select row_hash from target_table;

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