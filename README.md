# Running ETL locally
This is a docker-compose file for **Gen3 ETL-related** containers that help developers running Gen3 ETL locally. Basically, there are two main containers:
1. Spark: that consists of HDFS and Spark instance that do the data transformation stage of ETL explained [here](https://github.com/uc-cdis/tube).
2. Tube: that consists of [Gen3 Tube](https://github.com/uc-cdis/tube) that is a tool written in Python define the way that we do data transformation in Spark.

Two additional containers `ElasticSeach` and `Kibana` should be also installed if your local environment does not have ElasticSeach.

There are also multiple configurations in `configs` folder. `creds.json` stores the credential and connection setting to database, while `etlMapping.yaml` defines the expected index and the way to create from original database.
