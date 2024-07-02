# ADR-005 Choose data storage for matching service

Date: 2024-07-02

## Status

Accepted

## Context

We chose to make matching service with pipeline architecture style in [ADR-004](./004-Choose-pipeline-for-matching-service.md).

Now we should decide how to store data for this service.

Matching bounded context requires workers data and tasks data. Workers data could be unstructured while tasks data will be structured and extracted from RDBMS of other service.

## Decision

We choose to store our unstracture data as files in data lake while developers are free to choose relational/document/graph/column database to build a research on top of it. For the high availability of the service RDBMS is recommended.
