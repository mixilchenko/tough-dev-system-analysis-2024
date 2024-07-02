# ADR-002 Choose microservices architecture style

Date: 2024-07-02

## Status

Accepted

## Context

MCF project has 11 bounded contexts.

Subdomains and bounded contexts with their requirements and restictions are displayed on Apple Freeform and [shared with read-only access](https://www.icloud.com/freeform/0d9xpeideZwBge-FDn5wrhvog#MCF_Services)

We look at [architecture styles worksheet from DeveloperToArchitect.com](https://www.developertoarchitect.com/downloads/worksheets.html) to compare different approaches.
According to requirements, there are two styles that suit best

- service-based
- microservices

## Decision

Choose microservices architecture style to implement the project.

We are not able to make service-based approach with one database for all the services because there are requirements to divide contexts like betting and matching.

## Consequences

**Positive:**

- High quality of agility, deployability and testability.
- Higher independence between teams that are going to implement services.

**Negative:**

- Cost of development.
- Different architecture styles for different services.
