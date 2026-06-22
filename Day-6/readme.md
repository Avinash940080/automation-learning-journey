# Day 6 - Make.com Essentials

## Objective

Learn the fundamentals of Make.com and understand how its concepts compare to n8n.

---

## Concepts Learned

### 1. Custom Webhooks

* Created a custom webhook in Make.
* Used the webhook URL to receive data from Hoppscotch.
* Learned that webhooks act as endpoints that listen for incoming HTTP requests.

### 2. HTTP Module

* Used the HTTP module to send GET requests to external APIs.
* Connected the webhook data to the HTTP module using mapping.
* Used the Agify API to predict age based on a given name.

Example:

Input:

```json
{
  "name": "Avinash"
}
```

API Response:

```json
{
  "name": "Avinash",
  "age": 35,
  "count": 1948
}
```

### 3. Mapping Data

* Learned how to map data from one module to another.
* Passed the `name` field received by the webhook into the HTTP request query parameter.

### 4. Filters

* Learned that Make.com uses Filters instead of IF nodes.
* Added conditions directly on connections between modules.

Example:

```
age > 30
```

### 5. Routers

* Learned how Routers create multiple workflow branches.
* Built separate paths for different conditions.

Example:

```
Age > 30
Age <= 30
Age is Empty
```

### 6. Gmail Integration

* Connected a Gmail account.
* Sent emails based on filter conditions.
* Used different email templates for different branches.

### 7. Handling Missing Data

* Discovered that some names return empty age values from Agify.
* Added a dedicated branch to handle missing data.
* Learned the importance of handling edge cases in automations.

---

## Comparison with n8n

| n8n               | Make.com       |
| ----------------- | -------------- |
| Node              | Module         |
| Webhook           | Custom Webhook |
| HTTP Request      | HTTP Module    |
| IF Node           | Filter         |
| Multiple Branches | Router         |
| JSON Output       | Bundle         |
| Expressions       | Mapping        |

---

## Key Takeaways

* Make.com and n8n use different interfaces but follow the same automation concepts.
* Understanding automation fundamentals is more important than learning a specific platform.
* Data mapping is the foundation of workflow automation.
* Edge cases and missing data must always be considered.
* A working automation should handle both successful and unexpected scenarios.

---

## Status

✅ Custom Webhooks

✅ HTTP Module

✅ Data Mapping

✅ Filters

✅ Routers

✅ Gmail Integration

✅ Error Handling

✅ Make.com Fundamentals Completed
