# HW4

## Where to start

I do not choose hw0 as a start point because I left too many parts of the system out of MVP (see [v0 description](../v0/Description.md)).

I choose my hw1 as a start point since it was pretty raw and unplanned. 

According to [v1 implementation document](../v1/implementation.md) there are only

- billing as a separate service
- other things placed into monolyte

## Services achanges in hw3

"other things" were renamed to Help Service with extraction of

- Matching
- Betting
- Workers Testing
- FinData

Except that HCB testers copying and Fur-tune cookies are two external services we use as well.

Also according to comments from reviewers, FinData should be splitted to

- workers payments
- clients payments

## Instability

In hw1 there was connection from "other things" service to billing because billing requires data about clients, tasks, managers.

This means that "other things" service has 0 afferent coupling and 1 efferent coupling so instability is 1.

Billing has 1 afferent coupling and 0 efferent couplint so instability is 0.

## How to work to change the system

### Experience, infrastructure, no resources

We should start with services that could make the profit first.

I would say that workers testing service is the important part here so we could hire qualified cats.

Matching should be the second priority. It is the core part of the system and requires high modifiability so extracting it to separate service could speed up researchers work.

Billing could be next due to CatFinCompliance if service does not meet the requirements. If it meets the requirements right now, we could split it to clients payments and workers payments as the last step.

Next we should extract betting because top-management wants to hide it from other system parts.

### Resources, no experience and infrastructure

We should start with the easiest parts of the system.

I would say that the easiest part is to extract betting because it has very ow coupling and does not seem to be a complex system.

Then we could do workers testing service. It has low coupling as well.

The third part would be Billing splitting. It requires to make separate database and start the work on dividing the code.

The last but not least is matching - the most complex part of the system.
