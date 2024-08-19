Converting DynamoDB to PostgreSQL

Row-level/Row-based security
Easier to change shape of data

DynameDB is schema-less so changing structure often involves changing application code. Also you can't use codegeneration tools like PostGraphile. Easier data migration, you can add a column with a default and not need to modify each row necessarily.

JSON sql types are great for unstructured data. User preferences, feature flags


Hoppin World's ETL

1) User Uploads Video to S3 Bucket (New Content)
2) On file upload finished, sends event to SQS queue
3) SQS Queue activated a Lambda function that would initiate the Hybrik Jobs
	1) Multilple jobs were created for different file formats
4) Lambda function would also listen for Hybrik updates to record progress and errors in the database
5) After all jobs were completed, raw video file was moved to another S3 bucket with slower cheaper access

Hoppin ElasticSearch
- Used to optimize search queries for shared Experiences and Scenes
- Also used for user search to show the most popular and relevant searches
- ElasticSearch works well with Mongodb since you can index unstructured data


Autocorp stuff
- AWS CDK
	- Tooling to create new Lambda layers
- Cloudflare Edge Computing
- Postgraphile