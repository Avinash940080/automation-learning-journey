# Day 5: Authentication, API Keys, and Real-World APIs

## Objective

Understand how APIs secure access to their services and build a workflow that integrates with a real-world API.

## Project

Built an event-driven workflow that receives a webhook request, fetches a random quote from a public API, and sends it via Gmail.

## Workflow Overview

Webhook
↓
HTTP Request (ZenQuotes API)
↓
Gmail

## Business Logic

1. Receive a trigger through a webhook.
2. Request a random quote from the ZenQuotes API.
3. Extract the quote and author from the API response.
4. Send the quote to an email recipient.

## Tools Used

* n8n
* Hoppscotch
* ZenQuotes API
* Gmail

## Concepts Learned

### Authentication

Authentication verifies the identity of an application before granting access to an API.

Common authentication methods:

* API Keys
* Bearer Tokens
* OAuth

### API Keys

API keys are secret credentials used to access protected APIs.

Best practices:

* Never commit API keys to GitHub
* Never include API keys in screenshots
* Store API keys in n8n credentials

### HTTP Headers

Headers provide additional information with API requests.

Example:

Authorization: Bearer YOUR_API_KEY

### Public vs Private APIs

* Public APIs can be used without authentication.
* Private APIs require credentials.

### JSON Arrays

Unlike previous APIs that returned JSON objects, the ZenQuotes API returned an array.

Example:

[
{
"q": "The best way to get started is to quit talking and begin doing.",
"a": "Walt Disney"
}
]

This required accessing data using array indexes.

Examples:

* `{{ $json[0].q }}`
* `{{ $json[0].a }}`

## Challenges Faced

* Understanding API authentication and billing
* Learning the difference between public and private APIs
* Encountering API quota limitations
* Understanding JSON arrays versus JSON objects

## Key Learnings

* APIs often require authentication.
* API usage may have quotas and billing limits.
* HTTP headers carry authentication information.
* API responses can have different JSON structures.
* Developers must inspect API responses before building workflows.

## Key Takeaway

Receive data → Call an API → Parse JSON → Take action.
