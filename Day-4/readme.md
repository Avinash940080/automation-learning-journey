# Day 4: APIs, Webhooks, and HTTP Requests

## Objective

Understand how applications communicate over the internet and build an event-driven workflow using webhooks and APIs.

## Project

Built a workflow that receives data through a webhook, calls an external API, evaluates the response, and sends different emails based on the result.

## Workflow Overview

Webhook
↓
HTTP Request (Agify API)
↓
IF Age > 30
├── True → Gmail
└── False → Gmail

## Business Logic

1. Receive a person's name through a webhook.
2. Send the name to the Agify API.
3. Receive the predicted age.
4. If the predicted age is greater than 30, send one email.
5. Otherwise, send a different email.

## Tools Used

* n8n
* Hoppscotch
* Agify API
* Gmail

## Concepts Learned

### HTTP

HTTP is the communication protocol used by applications over the internet.

Common methods:

* GET: Request data
* POST: Send data

### APIs

APIs allow applications to communicate and exchange data.

### Webhooks

Webhooks are URLs that receive data automatically when an event occurs.

### Request and Response

Applications communicate by sending requests and receiving responses.

### JSON

Data exchanged between applications is commonly represented as JSON.

### Expressions

Examples:

* `{{ $json.body.name }}`
* `{{ $json.age }}`

### Conditional Logic

Used an IF node to create branching workflows based on API responses.

## Challenges Faced

* Understanding the difference between APIs and webhooks
* Learning GET vs POST methods
* Understanding JSON structures from different nodes
* Debugging webhook test mode
* Resolving Gmail node expression errors
* Fixing workflow synchronization issues

## Key Learnings

* HTTP is the language of communication.
* APIs expose functionality using HTTP.
* Webhooks receive event-driven data.
* n8n orchestrates data flow between applications.
* Different nodes produce different JSON structures.

## Key Takeaway

Receive data → Process data → Call an API → Make a decision → Take action.
