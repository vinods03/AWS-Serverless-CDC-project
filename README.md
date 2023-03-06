Please refer the Architecture diagram to understand what we are trying to achieve.  
0. RDS Source Data - Full load (initial data).txt is the initial data setup that needs to be done on the RDS MySQL database.  
2. RDS Source Data - Changes.txt are the changes / additions done on the initial data on the RDS MySQL database.  
The DMS service is set to migrate existing data and replicate ongoing changes.  
All the loads / changes done on the RDS MySQL database will be captured on the S3 data lake.  

We are not using Redshift for storage or EMR for processing.  
S3 is used for storage and glue jobs for processing. DynamoDB is being used to capture audit information.  
