
## Architecture

***Note*** - *My Agentic network location is under registries/generated/jira_tickets_router.hocon*

### Overview

This project uses a hierarchical Agentic AI architecture to classify and route Jira tickets. A Supervisor Agent acts as the entry point and delegates tickets to the appropriate team. If the selected team contains sub-teams, the request is further routed to the most relevant sub-team agent, which generates the final response.

### Agent Architecture

```text
                    +------------------+
                    | Supervisor Agent |
                    +------------------+
                              |
        ------------------------------------------------
        |                |               |             |
       SAP      Data Analytics      Finance    Power Automate
        |                |               |             |
     ----------     ----------------   --------    ---------------
     |        |      |      |      |   | | | |     |             |
    BW       SAC   Power BI Qlik Vertica FI CO MM SD Cloud Flow Desktop Flow
```

### Routing Flow

```text
Incoming Jira Ticket
        │
        
Supervisor Agent
        │
        
Team Agent
        │
        
Sub-Team Agent
        │
        
Final Response
```



### Workflow

1. A Jira ticket is submitted.
2. The Supervisor Agent identifies the appropriate team.
3. The Team Agent routes the ticket to the correct sub-team.
4. The Sub-Team Agent analyzes the issue.
5. The Sub-Team Agent returns a concise solution in one or two sentences.

### Design Highlights

* Hierarchical multi-agent architecture.
* Modular team and sub-team routing.
* Easy to extend with new teams and domains.
* Clear separation of responsibilities between agents.
