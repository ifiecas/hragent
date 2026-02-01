#Self-Service Employment Certificate Generator

This repository contains a Copilot Studio HR agent that generates employment certificates using AI, grounded in company data stored in SharePoint.

The goal of this project is to show how AI can help pre-fill business documents while keeping all factual information controlled, accurate, and safe for real-world use.

What This Does

This HR agent lets employees generate their own employment certificate in minutes.

No HR emails

No manual document editing

No waiting

AI helps with wording and structure, while employee data comes from a SharePoint list as the single source of truth.

How It Works

An employee opens the HR agent and requests an employment certificate.

The system:

Identifies the logged-in user

Looks up employee details in SharePoint

Uses AI to generate the document wording

Pre-fills a fixed Word template

Converts the document to PDF

Returns a download link

All of this happens in one automated flow.

Architecture

At a high level, the flow looks like this:

Copilot Studio (HR Agent)
  → Power Automate
  → SharePoint List (Employee Data)
  → Word Template (Pre-fill)
  → PDF Conversion
  → SharePoint Library
  → Download Link returned to Copilot


SharePoint is the source of truth.
AI never invents employee information.

Key Principles

AI is used for structure and wording only

All employee data is retrieved from SharePoint

Documents always follow a fixed template

Output is consistent and company-ready

This keeps AI-generated documents controlled and reliable.

What’s Included

Copilot Studio package export

Power Automate flow definitions

Example SharePoint list schema

Sample Word employment certificate template

Where This Pattern Applies

This same approach works for any document that is created regularly using a template, such as:

Employment certificates

Contracts

Statements of work

Invoices

Internal letters

Newsletters

Once the structure and data sources are in place, AI can help generate documents at scale.

Notes

Employee data in this repo is simulated

Templates can be replaced with company-branded versions

Approval steps and signatures can be added if needed

Credits

Inspired by Matthew Devaney’s talk on grounding AI-generated documents in company data:
https://www.youtube.com/watch?v=g6SsJdbgSeM
