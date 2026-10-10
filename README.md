# Automated Email Ticketing & Routing System

## Overview

An automated email ticketing and routing system built using n8n, Gmail, Notion, and Slack.

The project processes incoming customer emails, categorizes requests using predefined rules, creates support tickets in Notion, notifies the appropriate team, and sends customer confirmation emails.

A separate error-handling workflow is configured to send Slack alerts when workflow executions fail.

## Technologies Used

- n8n
- Gmail
- Notion
- Slack
- OAuth 2.0
- Workflow Error Trigger

## Main Workflow

1. Receive incoming customer emails through Gmail.
2. Extract customer details and email content.
3. Classify requests using keyword-based routing.
4. Create categorized tickets in Notion.
5. Notify the team through Slack.
6. Send a confirmation email to the customer.

## Error Handling Workflow

A separate n8n workflow uses an Error Trigger connected to Slack.

The notification is configured to include:

- Workflow name
- Failed node
- Error message
- Execution URL

## Workflow Architecture

**Main Workflow**

Gmail Trigger → Prepare Email Data → Classify Request → Create Notion Ticket → Slack Notification → Gmail Confirmation

**Error Handler**

Error Trigger → Slack Admin Notification

## Project Files

- `Automated Email Ticketing & Routing System.json` — Main workflow
- `Email Ticketing - Error Handler.json` — Error monitoring workflow

## Key Features

- Automated email intake
- Keyword-based request classification
- Notion ticket management
- Team notifications through Slack
- Customer confirmation emails
- Separate error monitoring workflow

## Project Status

Core workflows implemented and exported. End-to-end validation and error notification testing should be completed before production deployment.

## Future Improvements

- AI-powered email classification
- More robust email address extraction
- Duplicate ticket prevention
- Priority-based routing
- Improved customer confirmation handling
- Reporting and analytics

## Security

Credentials must be configured separately in n8n. Do not publish access tokens, API keys, or real customer information.
