# ADR-003 Divide services

Date: 2024-07-02

## Status

Accepted

## Context

We chose microservices architecture style according to [ADR-002](002-Choose-microservices-architecrute-style.md).

Now we should decide which services we have for our 11 bounded contexts.

## Decision

### No service

`HCB testers copying` and `Fur-tune cookies` contexts that do not require services because they are external.

`Worker helping clients` does not require service because this context describes how worker is doing his work for the client task.

### FinData service

`Clients Payments` and `Workers Payments` are two contexts that require high consistency and non-modifiability of data according to CatFinCompliance.

### Matching service

`Matching` context is a separate service so we are able to develop it with high modifiability as a context in core subdomain.

### Workers Testing service

`Tests and reviews` context is a separate service so we are able to develop it with high modifiability as a context in core subdomain.

### Betting service

`Betting` context is a separate service to divide it from all the other services according to managers concern

### Help service

`Visits planning`, `Consumables providing` and `Quality review` are three contexts that we do not need to divide because they have very similar requirements.
