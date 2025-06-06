# Decodable Examples

![Real-time Data: Simplified](https://img.shields.io/badge/real%E2%80%93time%20data-simplified-%232F74F9?labelColor=%2306091A&link=https%3A%2F%2Fdecodable.co)
![GitHub last commit](https://img.shields.io/github/last-commit/decodableco/examples)
![GitHub License](https://img.shields.io/github/license/decodableco/examples)
![Static Badge](https://img.shields.io/badge/we%20love-apache%20flink-%23E6526F?logo=apacheflink)

![A squirrel holding a laptop that says "Examples repo"](images/examples_repo.webp)

## Introduction

This repository contains examples of use cases that utilize Decodable streaming solution as well as demos for related open-source projects such as Apache Flink, Debezium, and Postgres.

Examples are presented "as-is" and are maintained on a best effort basis. PRs for updating existing (or adding new) examples are welcome!

For help with any of the examples, or using Decodable in general, please [join our Slack group](https://join.slack.com/t/decodablecommunity/shared_invite/zt-uvow71bk-Uf914umgpoyIbOQSxriJkA).

## About Decodable

_Decodable radically simplifies real-time data, making it easier to access the freshest, high-quality data. Reduce infrastructure overhead, connect data sources, transform, and deliver data reliably to any destination._

_Learn more [here](https://decodable.co), and [sign up for a free trial](https://app.decodable.co/-/accounts/create) today!_

## Contents

### Stream Processing Techniques

| Example                                     | Description                                                                                                    |
|---------------------------------------------|----------------------------------------------------------------------------------------------------------------|
| [Change Streams](change-streams)            | Using change streams to build materialized views in Postgres                                                   |
| [XML Processing](xml)                       | Parse XML and transform to JSON                                                                                |
| [Masking](masking)                          | Ways to mask data                                                                                              |
| [Array Aggregation (1)](array-agg-postgres) | Demonstrating how to aggregate the elements of the many side of 1:n join into an array with data from Postgres |
| [Array Aggregation (2)](array-agg)          | Using the `array_agg()` UDF for denormalizing data in a pipeline from MySQL to OpenSearch                      |

### Data Pipelines

| Example                                                 | Description                                                                            |
|---------------------------------------------------------|----------------------------------------------------------------------------------------|
| [Opinionated Data Pipelines](opinionated-pipelines)     | Building data pipelines with schema on write streams.                                  |
| [Postman](postman)                                      | Building data pipelines with Postman.                                                  |
| [Postgres to Snowflake](postgres-to-snowflake-with-cdc) | Getting data from Postgres to Snowflake using Decodable.                               |
| [Flink CDC](flink-cdc)                                  | Trying out Flink CDC and comparing it to Flink SQL.                                    |
| [Flink SQL and Custom Pipelines](sql-cupi-hybrid)       | Bridging Flink SQL and Custom Java Pipelines with the Decodable SDK.                   |
| [Testing Custom Pipelines on Decodable](testing-cupi)   | How to write more modular Flink jobs with pluggable components to improve testability. |


### PyFlink

_Decodable provides a managed PyFlink service. Learn more [here](https://docs.decodable.co/pipelines/create-pipelines-using-your-own-apache-flink-jobs.html#_create_a_custom_pipeline_python)._

| Example                                                         | Description                                                                             |
|-----------------------------------------------------------------|-----------------------------------------------------------------------------------------|
| [PyFlink](pyflink)                                              | Running a basic PyFlink job on Kubernetes                                               |
| [PyFlink on Decodable](pyflink-decodable)                       | Running a PyFlink job as a Custom Pipeline on Decodable                                 |
| [PyFlink and MongoDB Vector Search](pyflink-vector-embeddings)  | End-to-end example for PyFlink Vector Ingestion on Decodable with MongoDB Vector Search |
| [PyFlink Intro](pyflink-intro)                                  | A Hands-On Introduction to PyFlink                                                      |

### Integrations

| Example                                                                    | Description                                                                                                                                                                                                          |
|----------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------|
| [Apache Druid](druid)                                                      | Sending COVID-19 data to Decodable using its REST API, cleaning it with SQL, and then sending it to Apache Druid      |
| [Apache Kafka / Flink / Iceberg](kafka-iceberg/apache-flink)               | Integrating Apache Kafka with Apache Iceberg through Apache Flink. _As presented at Kafka Summit London 2024_         |
| [Apache Kafka / Flink / Iceberg](kafka-iceberg/decodable) (with Decodable) | Streaming from Apache Kafka to Apache Iceberg with Decodable                                                          |
| [Apache Kafka Upsert connector](kafka-upsert/)                             | Explaining the difference between the Flink Kafka and Kafka Upsert connectors                                         |
| [Apache Kafka mTLS](mtls)                                                  | Installing Apache Kafka on EC2 and configuring it with mTLS                                                           |
| [Apache Kafka with ngrok](kafka-ngrok)                                     | Using Docker Compose for running Apache Kafka locally, accessible from the internet using ngrok                       |
| [Apache Kafka](kafka2s3)                                                   | Installing Apache Kafka on EC2 and writing to S3 with Decodable                                                       |
| [Apache Pinot](pinot)                                                      | Transforming osquery logs to Apache Pinot and Superset                                                                |
| [AsyncAPI](asyncapi)                                                       | Publishing Data Products with AsyncAPI                                                                                |
| [Confluent](confluent)                                                     | Clickstream from Confluent Cloud joined with CDC user data from Postgres                                              |
| [Delta Lake / Flink](flink-delta-lake)                                     | Writing to Delta Lake with Apache Flink                                                                               |
| [GitHub Webhooks](github-webhooks)                                         | Processing GitHub Webhook events using the Decodable REST source connector                                            |
| [OSQuery Routing](osquery)                                                 | Routing OSQuery logs with SQL                                                                                         |
| [Redpanda](redpanda)                                                       | Reading and writing data to Redpanda from Flink                                                                       |
| [S3 Events in a Lambda Function](s3events/)                                | Configuring an S3 bucket with a Lambda notification to send data to Kinesis to be processed in Decodable              |
| [Tinybird](tinybird)                                                       | Writing data to Tinybird from Decodable                                                                               |

### Changed Data Capture (CDC)

| Example                                                          | Description                                                                                                          |
|------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------|
| [MSSQL CDC](mssql_cdc/)                                          | Enabling MSSQL in Docker with CDC, reading from it with Debezium, writing change events into AWS Kinesis             |
| [Oracle CDC](oracle_cdc/)                                        | Configuring Oracle AWS RDS with LogMiner, reading from it with Debezium, writing change events into AWS Kinesis      | 
| [DynamoDb CDC](dynamodb_cdc/)                                    | Configure DynamoDB to send change data to Kinesis, reading changes into Decodable for transformation or replication. |
| [Logical Decoding Message Examples](postgres-logical-decoding)   | How to retrieve logical decoding messages from the Postgres WAL                                                      |
| [Logical Replication on Postgres 16 Stand-By Servers](postgres-logical-replication-standby) | How to use logical replication on Postgres 16 stand-by servers                            |
| [Postgres 17 Fail-Over Slots](failover-slots)                    | How to use fail-over slots with Postgres 17                                                                          |
| [Transactional CDC Event Aggregation](tx-aware-cdc-buffering)    | Aggregating Change Data Capture Events based on Transactional Boundaries                                             |

### Flink SQL

| Example                                               | Description |
|-------------------------------------------------------|-------------|
| [Flink SQL Troubleshooting](troubleshooting-flinksql) | A set of Docker Compose environments for demonstrating various Flink SQL troubleshooting scenarios (see [related blog](https://www.decodable.co/blog/flink-sql-misconfiguration-misunderstanding-and-mishaps?utm_medium=github&utm_source=examples_repo&utm_campaign=blog&utm_content=troubleshooting-flinksql))|

### Decodable tools

| Example                                               | Description |
|-------------------------------------------------------|-------------|
| [Decodable CI/CD](declarative-cicd) | An example of using Decodable with GitHub Actions|
| [Decodable CLI Docker image](cli-docker) | An example Dockerfile for running the Decodable CLI under Docker.|

### Kubernetes

| Example                                               | Description |
|-------------------------------------------------------|-------------|
| [Fink on Kubernetes](flink-on-kubernetes) | An example of running Flink via the Flink Kubernetes Operator|

## License

This code base is available under the Apache License, version 2.
