# Day 2: Airtable Deep Dive - Building a Lead Management CRM

## Objective

Learn how Airtable works as a relational database and understand how businesses organize customer information.

## Project

Built a Lead Management CRM using Airtable.

## Tables Created

### Leads

Stores information about potential customers.

Fields:

* Name
* Email
* Company
* Source
* Status

### Follow-ups

Tracks interactions with leads.

Fields:

* Follow-up Name
* Lead (Linked Record)
* Date
* Channel
* Notes
* Status

## Concepts Learned

### Base

A complete database project.

### Table

A collection of related data.

### Record

A single row of information.

### Field

A column that stores a specific type of data.

### Linked Records

Connected records between tables.

Relationship created:

One Lead → Many Follow-ups

### Views

Filtered ways to look at the same data.

Created:

* All Leads
* New Leads
* Qualified Leads

### Lookup Fields

Fields that automatically pull data from linked records.

## What is a CRM?

CRM stands for Customer Relationship Management.

Businesses use CRMs to track:

* Potential customers
* Communication history
* Follow-ups
* Sales progress

## What is a Lead?

A lead is a person or company that might become a customer.

Examples:

* Website inquiries
* LinkedIn messages
* WhatsApp conversations
* Referrals

## How Airtable Fits into Automation

Airtable often acts as the source of truth for workflows.

Example:

Website Form → Airtable → n8n → Email Notification

## Key Takeaway

Airtable is a relational database with a spreadsheet-like interface that integrates with automation tools like n8n and Make.
