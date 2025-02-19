# Issues or challenges

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