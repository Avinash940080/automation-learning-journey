# 🚀 Job Alert Automation

An automated multi-user job recommendation system built using **n8n**, **Airtable**, **JavaScript**, and **Gmail**.

---

## 📖 Overview

Job Alert Automation is an end-to-end workflow automation project that automatically collects job listings from a public Job API, stores them in Airtable, matches them with user preferences, and sends personalized HTML email recommendations.

The project demonstrates workflow automation, API integration, database operations, JavaScript-based filtering, and automated email generation using n8n.

---

# 🎯 Problem Statement

Searching multiple job portals every day is repetitive and time-consuming.

This project automates the process by:

* Collecting the latest job listings
* Storing them in a database
* Matching jobs with user preferences
* Delivering personalized job recommendations via email

---

# ✨ Features

* Multi-user support
* Automated job collection from a Job API
* Airtable database integration
* Role-based job matching
* Personalized HTML email generation
* Scheduled workflow execution
* Modular workflow architecture

---

# 🏗️ System Architecture

The project is divided into two independent workflows.

## Workflow 1 — Job Collector

Responsible for collecting jobs from the Job API and storing them in Airtable.

```text
Schedule Trigger
        │
HTTP Request (Job API)
        │
Split Job Records
        │
Format Data
        │
Create Record (Jobs Table)
```

---

## Workflow 2 — Job Matcher

Responsible for matching jobs with registered users and sending personalized emails.

```text
Schedule Trigger
        │
Fetch Users
        │
Fetch Jobs
        │
JavaScript Matching Logic
        │
Generate HTML Email
        │
Send Email (Gmail)
```

---

# 🛠️ Tech Stack

| Category            | Technology |
| ------------------- | ---------- |
| Workflow Automation | n8n        |
| Database            | Airtable   |
| Programming         | JavaScript |
| Email Service       | Gmail      |
| API Integration     | REST API   |
| Data Format         | JSON       |

---

# 📷 Project Screenshots

### Architecture

* System Architecture Diagram

### User Registration

* Airtable Form

### Database

* Users Table
* Jobs Table

### Workflows

* Job Collector Workflow
* Job Matcher Workflow

### Output

* Sample HTML Email

---

# 📧 Email Output

Each registered user receives a personalized HTML email containing:

* Matching Job Title
* Company Name
* Apply Link

---

# 🧠 Challenges Faced

* Designing a scalable workflow architecture
* Passing data between multiple n8n nodes
* Matching jobs with multiple users
* Generating personalized HTML emails
* Understanding workflow execution and data flow
* Debugging node expressions and Airtable integrations

---

# 📈 Future Improvements

* Automatic cleanup of outdated job listings
* Better duplicate job handling
* Location-based filtering
* Integration with additional Job APIs
* Resume-based AI job matching
* Telegram / WhatsApp notifications
* Analytics dashboard

---

# 📚 What I Learned

Through this project I learned:

* Workflow automation using n8n
* REST API integration
* Airtable CRUD operations
* JavaScript inside automation workflows
* JSON data processing
* Workflow architecture and scheduling
* HTML email generation
* Debugging automation pipelines

---

# 🚀 How to Run

1. Clone this repository.
2. Import the n8n workflow JSON files.
3. Create the required Airtable base with:

   * Users Table
   * Jobs Table
4. Configure Airtable credentials.
5. Configure Gmail credentials.
6. Execute the Job Collector workflow.
7. Execute the Job Matcher workflow.

---

# 📁 Project Structure

```text
Job-Alert-Automation/
│
├── README.md
├── LICENSE
├── .gitignore
│
├── workflows/
│   ├── job-collector.json
│   └── job-matcher.json
│
└── screenshots/
    ├── architecture.png
    ├── airtable-form.png
    ├── users-table.png
    ├── jobs-table.png
    ├── workflow-job-collector.png
    ├── workflow-job-matcher.png
    └── sample-email.png
```

---

# 👨‍💻 Author

**Avinash**

Built as a portfolio project to demonstrate workflow automation, API integration, database management, and personalized email automation using n8n.
