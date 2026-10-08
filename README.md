# Manufacturing ERP & Business Process Automation Case Study

> Portfolio case study. Source code, customer identity, screenshots, operational data, database design, API details and proprietary business rules are intentionally omitted.

## Overview

I am an AI and Business Systems Engineer based in Warsaw, Poland. I currently design and develop a production ERP system for a manufacturing business.

My role is not limited to software implementation. I learn how the business operates, map its workflows and responsibilities, identify manual or repetitive work, translate operational requirements into system behavior, and validate the resulting solution with real users and business scenarios.

The system currently supports approximately 20 users.

## Business Context

The project replaces fragmented processes spread across spreadsheets, email communication and manual operational checks.

The work requires understanding how information moves between planning, purchasing, sales, production, warehouse operations, shipments, invoicing and management reporting. These areas are connected, but each has its own permissions, lifecycle rules and validation requirements.

## My Responsibilities

- Business-process discovery and workflow analysis
- Requirements clarification with operational stakeholders
- Translation of business rules into technical behavior
- System and API architecture
- Backend and frontend implementation
- Database and integration design
- Role-based access control and application security
- Automated backend and frontend testing
- Browser-based end-to-end validation
- Deployment preparation and technical documentation

## Functional Scope

The ERP includes functionality across:

- Planning
- Purchase orders
- Customer orders
- Production and production usage
- Inventory
- Shipments
- Invoices
- Customers and products
- Pricing
- Dashboards
- User roles and permissions
- Notifications
- Activity and audit tracking
- In-application guidance

This list describes functional coverage only. Proprietary workflows, state transitions, formulas and implementation details are not published.

## Technical Foundation

- React 19 and JavaScript/JSX
- Python 3.11 and FastAPI
- MongoDB and Motor
- REST APIs
- Git and GitHub
- Playwright
- Automated frontend and backend test suites
- OpenAI Codex for agent-assisted engineering

The application uses security controls including HttpOnly cookie-based authentication, CSRF protection, Argon2id password hashing, role-based permissions, exact-origin CORS configuration, trusted-host validation and request throttling.

## Agent-Assisted Development

I use OpenAI Codex daily inside the development workflow for:

- Repository and dependency analysis
- Feature implementation
- Refactoring support
- Debugging
- Test generation
- Browser-based QA
- Regression analysis
- Code review
- Controlled Git delivery

AI-generated output is treated as an implementation proposal, not as automatically correct code. Business rules, security-sensitive behavior and user-facing workflows are reviewed and validated before release.

I have not yet integrated an OpenAI or Anthropic API directly into this ERP. My current AI experience is focused on production-level agent-assisted software development, architecture, debugging, testing and validation.

## Example: Catching an Agent-Generated Defect

During development of an invoice interface, I caught a data-binding error in code produced with Codex.

When a user changed the Secondary Qty value in an invoice row, the column heading changed as well. Manual workflow testing exposed the problem before release.

I traced the issue to the heading being incorrectly coupled to editable row-level data. The static heading was separated from transactional state, and the correction was verified in three places:

1. The frontend interface
2. The generated invoice PDF
3. Regression tests

The incident reinforced an important engineering rule: presentation labels must remain independent from editable transactional data, and invoice changes must be validated across every output that represents the same business document.

## Measurable Outcome

For selected inventory and production reporting activities, work that previously required days of manual counting and cross-checking can now be completed in approximately five minutes using live operational data and automated calculations.

## What This Project Demonstrates

- Understanding a business before designing its software
- Converting manual operational processes into reliable systems
- Connecting requirements, architecture and implementation
- Working across ERP modules with real business dependencies
- Building secure internal tools with role-based access
- Using AI coding agents with human review and validation
- Testing changes across interfaces, APIs and generated documents
- Owning delivery from discovery through deployment preparation

## Confidentiality

This repository contains no source code, customer name, screenshots, credentials, operational records, database schema, endpoint definitions, infrastructure identifiers or proprietary business rules.

It exists solely to document the engineering approach, responsibilities and verified outcomes of the project.
