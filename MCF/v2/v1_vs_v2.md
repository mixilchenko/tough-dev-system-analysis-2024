# HW1 and HW2 comparison

## ES

In [HW1](/MCF/v1) there were 5 groups

- Tasks - the main workflows of the system
- Hire - Something to add workers to the system
- Managers - things that could be described as "managers have their admin panel
- Billing - invoices, payments
- Betting - our "managers motivation"

With [DDD approach in HW2](DDD.md) I distinguished more subdomains and bounded contexts

- Clients attraction
  - HCF testers base
- Workers attraction
  - Tests and reviews
- Help for clients
  - Tasks
  - Matching
- Support
  - Quality review
- Consumables for help
  - Consumables department
- Billing
  - Balance evaluation methodologies and Payments processing
- Clients loyalty
  - Cookies with predictions
- Managers motivation
  - Betting

1. Clients attraction subdomain was totally missed.
2. Hire ES context was covering Workers attraction subdomain which is fine
3. Tasks ES context was covering 3 subdomains with 4 bounded contexts
   1. Help for clients
   2. Consumables for help
   3. Clients loyalty
4. Managers ES context was covering Quality review bounded context along with some parts of other bounded contexts - the worst partition here
5. Billing ES context was covering Billing subdomain with one bounded context whih is correct
6. Betting ES context was covering betting bounded context which is correct

## Data Model

To be fair data model diagram became more complicated with more connections. Maybe this highlights that I missed lots of connection in HW1 or maybe my new bounded contexts are not good enough.
