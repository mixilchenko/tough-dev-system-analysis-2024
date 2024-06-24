# Domain Driven Developmant

## Subdomains

### Clients attraction

Subdomain to find clients for the system.

For now the solution is to take only HCB cats-testers.

Could be high complexity and often changes in future when we are ready to scale and provide the service to any clients.

### Workers attraction

Subdomain to find top 3% workers.

Candidates are going to apply via some form. Managers are going to prerate and provide tests and then review the results.

### Help for clients

Subdomain for all of the tasks clients could create for workers to complete.

The biggest subdomain covering our business purpose.

For the solution we probably need

- task management
- algorithm to match workers to tasks
- task work

### Support

Subdomain for the done tasks review and clients help.

### Consumables for help

Subdomain that is responsible for the consumables required for each task.

### Billing

Subdomain to earn money.

The solutions here are

- payments processing to take money from clients and to provide money for workers
- Evaluation methodologies like fines processing for failed tasks

### Clients loyalty

Subdomain to increase clients loyalty.

Cookies with future predictions is the way.

### Managers motivation

Subdomain to increase managers motivation. 

Betting system is the way.

## Subdomains table to understand types

| Subdomain | Competitive advantage | Complexity | Changeability | Type |
|-|-|-|-|-|
|Clients attraction|yes|low|rare|Supporting|
|Workers attraction|yes|high|often|Core|
|Help for clients|no|high|often|Core|
|Support|no|high|rare|Supporting|
|Consumables for help|no|high|rare|Supporting|
|Billing|no|high|rare|Generic|
|Clients loyalty|no|low|rare|Generic|
|Managers motivation|no|low|rare|Generic|
