# ADR-004 Choose pipeline architecture style for matching service

Date: 2024-07-02

## Status

Accepted

## Context

We chose to make `Matching` bounded context as one separate service in [ADR-003](./003-Divide-services.md).

Now we should decide which architecture style we choose for this service.

## Decision

We are going to use pipeline architecture style because this suits best for the research purposes.
