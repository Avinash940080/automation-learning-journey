# Day 3: n8n Essentials – Building Conditional Automations

## Objective

Learn how data flows through n8n workflows and build an automation that makes decisions based on business logic.

## Project

Built a lead qualification workflow using Airtable, n8n, and Gmail.

## Workflow Overview

```text
Airtable Trigger
        ↓
IF Status = Qualified
       / \
   True   False
     ↓       ↓
 Gmail 1  Gmail 2
```

## Business Logic

* When a new lead is added to Airtable, the workflow starts.
* If the lead's status is `Qualified`, send a notification email.
* If the lead's status is anything other than `Qualified`, send a different notification email.

## Tools Used

* Airtable
* n8n
* Gmail

## Concepts Learned

### Triggers

A trigger starts a workflow when a specific event occurs.

Example:

* New record created in Airtable

### Nodes

Each step in an n8n workflow is called a node.

Nodes used:

* Airtable Trigger
* IF
* Gmail

### JSON

Data moves between nodes as JSON objects.

Example:

```json
{
  "fields": {
    "Name": "Avinash",
    "Email": "avinash@example.com",
    "Status": "Qualified"
  }
}
```

### Expressions

Expressions are used to access data from previous nodes.

Example:

```javascript
{{ $json.fields.Status }}
```

### Conditional Logic

The IF node enables branching based on conditions.

Example:

```text
If Status = Qualified → True branch
Else → False branch
```

### Polling Triggers

The Airtable Trigger uses polling.

Instead of listening continuously, it checks Airtable periodically for new records.

## Challenges Faced

* Understanding how data is structured in JSON
* Learning the difference between `Fetch Test Event` and `Execute Workflow`
* Debugging Airtable Trigger behavior during testing
* Understanding that editing existing records does not trigger new executions
* Discovering that trigger nodes can retain previous test state during development

## Solutions Implemented

* Used expressions to access dynamic data
* Tested workflows using newly created Airtable records
* Recreated the Airtable Trigger node to reset its internal state
* Verified workflow behavior using separate executions for True and False branches

## Key Learnings

* Triggers create data.
* Data flows between nodes as JSON.
* Expressions extract values from JSON.
* Conditions enable branching logic.
* Action nodes perform tasks based on workflow decisions.

## Key Takeaway

A trigger creates data, data flows as JSON, expressions access the data, conditions make decisions, and actions perform tasks.
