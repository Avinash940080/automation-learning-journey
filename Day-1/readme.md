# Day 1: Airtable to n8n Automation 

# Objective

Build my first workflow automation using Airtable and n8n.

The goal was to automatically send an email notification whenever a new lead is added to an Airtable table.

# Workflow

```text
Airtable Trigger → Gmail
```

When a new record is created in Airtable, n8n detects the event and sends an email notification.

# Tools Used

* Airtable
* n8n
* Gmail
* GitHub

# Airtable Setup

# Base

`Learning Automation`

# Table

`Leads`

# Fields

* Name
* Email
* company
* Status
* Created At

# Key Concepts Learned

* Triggers and actions
* Event-driven workflows
* Airtable Personal Access Tokens
* API authentication
* JSON structure and nesting
* Data mapping in n8n

# Understanding the Trigger

I learned that trigger nodes respond only to **new events**, not existing data.

For this workflow:

* `Created At` is used as the trigger field.
* Existing records are ignored.
* New records added after the trigger starts listening activate the workflow.

# JSON Example

Example data received from Airtable:

```json
{
  "fields": {
    "Name": "Test User",
    "Email": "test@example.com",
    "company": "Demo Company",
    "Status": "new"
  }
}
```

Example expressions used in n8n:

* `{{ $json.fields.Name }}`
* `{{ $json.fields.Email }}`
* `{{ $json.fields.company }}`
* `{{ $json.fields.Status }}`

# Challenges Faced

* Creating and configuring Airtable access tokens
* Understanding Base IDs and Table IDs
* Learning the difference between trigger events and existing records
* Configuring the correct trigger field
* Understanding JSON paths and data mapping

# Screenshots

The following screenshots are included in the `screenshots` folder:

* Airtable table setup
* Airtable Trigger node output
* Complete n8n workflow
* Gmail notification

# Key Takeaways

* Most automations follow a simple pattern:

```text
Trigger → Process Data → Action
```

* Triggers react to events.
* JSON data can be accessed using expressions.
* Documentation is an important part of building a portfolio.

# Next Steps

* Build the same workflow in Make.com
* Learn webhooks and APIs
* Create multi-step workflows
* Explore AI integrations
