# MCF - make cats free

## Problem

Cats do ot have enough time to cover their non-work needs.

## Company aim

Provide a platform where cats-clients could request service while cats-workers could provide it.

## Platform

### Roles

#### Manager

- CRUD service type in admin panel
- Configure tests for vacancies and specific cats
- Contact cat-worker candidate to provide tests
- Assigns characteristics to cats-workers
- Quality assurance of requests
  - Some done
  - All failed and canceled
- Contact client to
  - Request feedback
  - Help with failed, canceled requests
- Fill quality assurance form
- Deposit money for specific cat-worker
- Bet on request result

#### Cat-Client

- Request service via app
  - "Request Help" button procedes to form with
    - Service type
    - Description
    - Cost estimation
    - Phone
    - Email
    - Place
    - Comfortable datetimes
- Change status of request to one of
  - Done
  - Canceled
  - Failed
- Pay for the request (invoice on sunday)
- Sign done report for cat-worker (on paper)

#### Cat-Worker Candidate

- Apply on website

#### Cat-Worker

- See list of assigned requests
  - Active
  - Done
  - Canceled
  - Failed?
- Receive consumables for the work
- Arrive to place at specified time
- Change status of request to (conflicts with US-030)
  - Started
- Attach photo that work started
- Give done report to client for the signature
- Connect "Golden Hat" account

#### Consumables department

- Receive information what is required for the request
- Prepare for request
- Provide to cat-worker

### Systems

#### Cost estimator

- Estimate cost for the request form view (before matching)
- Estimate cost for the request after match
  - Get match
  - Evaluate cost (100 constant as MVP)
  - Get discount by client id

#### Matcher

- Connect client and worker based on request (random as MVP)

#### Cats-Workers System

- Save cats-workers information
  - Name
  - Age
  - Breed
  - Color
  - Photo
  - Characteristics decoded to 20 character string (US-101 but why?)
  - Is declined

#### App

- Send notification
  - cats-workers candidates flow
  - request status change
  - consumables are ready
  - invoices
  - quality assurance report
- Requests view
- Invoices view

#### Billing

- Generates invoices
- Sends emails

## Decisions

### How to choose

We are taking fast Time To Market as priority.
To achieve the result it is better

- to choose some important features leaving some user stories out of MVP scope
- to make monolite instead of multiple services

We are going to leave big user stories like US-150 and US-250 out of MVP scope. These requirements exist to cover motivation and users happiness which is too early without the product.

In future on some development iteration we could make microservice architecture because I could see separate modules like "Cost Estimator" and "Matcher". For now there are only stubs that are doing their work (fixed price and random match respectfully) and it is hard to predict which sophisticated data/interaction is required.

### What we need from MVP

- Developers are able to provide admin panel access to managers
- Anonyms are able to register as cats-clients
- Anonyms are able to request registration as cats-workers
- Managers are able to see cats-workers registration requests
- Cats-clients are able to create requests
- Cats-clients are able to see requests
- Cats-clients are able to cancel request
- Cats-clients are able to mark request done/undone 
- Cats-workers are able to see assigned requests
- Cats-workers see consumables department contacts to collect consumables
- Billing service is able to generate invoices
- Cats-clients are able to pay for the invoice
- Cats-workers are able to connect "Golden Hat" account
