# Event storming

## Note

I did the ES diagram in Freeform App.

There is a [read-only link to Freeform](https://www.icloud.com/freeform/019L9cWJtrWKrOBMvOmj_e0nw#MCF_v1_Event_Storming).

In case you are not able to join the board via icloud, PDF snapshot is attached in the pull request.

During this description I would try to use same colors that I have in diagram so it is easy to read.

## Actors and Events

I started with descriding <span style="color:#FAE27E">actors</span> and <span style="color:#F3B249">events</span>. Mostly I just went through user stories skipping some of them.

I distinguished some main <span style="color:#FAE27E">actors</span> during this step

- <span style="color:#FAE27E">Manager</span>
- <span style="color:#FAE27E">Client</span>
- <span style="color:#FAE27E">Worker</span>

Except them there are some extra <span style="color:#FAE27E">actors</span> and <span style="color:#ED756E">external systems</span>

- <span style="color:#FAE27E">Anon</span> - someone to apply for worker vacancy
- <span style="color:#FAE27E">Worker Candidate</span> - someone to complete tests after applying for worker vacancy
- <span style="color:#ED756E">Cookies service</span> - adds a cookie for each client task
- <span style="color:#ED756E">Consumables department</span> - prepares things for each client task
- <span style="color:#ED756E">Golden hat system</span> - processes worker payments

On some late steps I also added <span style="color:#FAE27E">Senior Manager</span> which manages betting

## Commands

Mostly it was easy to add a <span style="color:#84D7FB">command</span> because it is just another tense of the <span style="color:#F3B249">event</span>.

## Policies and Read Models

To add <span style="color:#97DC97">read models</span> I tried to understand what information <span style="color:#FAE27E">actor</span>/<span style="color:#ED756E">external system</span> needs to do specific <span style="color:#84D7FB">command</span>. I found these <span style="color:#97DC97">read models</span>.

- Tasks
  - Done/Undone/Failed/Canceled
  - Paid/Unpaied
- Tests
  - for candidates
  - to check
- Unprocessed candidates
- Invoices
- Bets

Seems that maybe I missed <span style="color:#FAE27E">"System" actor</span> and <span style="color:#97DC97">"Workers" read model</span> because this is something the matching system.
Instead in my diagram <span style="color:#F3B249">"Worker matched to task" event</span> is something that is produced from <span style="color:#FAE27E">"Client" actor</span> <span style="color:#84D7F8">"Create task" command</span>.

## Grouping

After my diagram was ready I made 5 groups

- Tasks - the main workflows of the system
- Hire - Something to add workers to the system
- Managers - things that could be described as "managers have their admin panel
- Billing - invoices, payments
- Betting - our "managers motivation"

## Communications

It is very strange that in my diagram there are no cross-context links.

"Billing" context uses information about the tasks but tasks changes do not trigger anything like invoices so I assume this is correct.

Task done status change could trigger

- manager to review task in "Managers" context
- senior manager to pay for the bets in "Betting" context

I am going to cover this in communication diagram but not in ES one.
