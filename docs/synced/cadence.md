---
title: Cadence
stack: FastAPI, Python, PostgreSQL, SQLAlchemy, Alembic, Pydantic, Jinja2, Docker, Uvicorn, pytest
date: "Not Specified"
---

## What the Project Does

Cadence is a managed subscription billing engine designed for Nigerian developers, built on top of Nomba's payment APIs. It addresses a critical infrastructure gap where local developers are forced to build complex recurring billing systems, state machines, and retry schedulers from scratch. 

Key capabilities of Cadence include:
- **7-State Billing Machine**: Manages subscription lifecycles robustly.
- **Automated Dunning**: Decoupled scheduler to handle failed payments and retries.
- **Double-Charge Protection**: Safeguards transactions against duplicate charges.
- **Hosted Self-Service Portal**: Allows end-users to manage their own subscriptions.
- **Multi-Tenancy**: Supports multiple independent tenant architectures.

## How It Is Built

Cadence acts as an orchestration layer between software applications and Nomba's payment primitives. The system architecture is designed for reliability and performance separation:
- **Web Layer**: Built with FastAPI, Pydantic, and Uvicorn to manage subscription states, process tokenized card authorizations, and dispatch webhooks.
- **Database Layer**: Powered by PostgreSQL, with SQLAlchemy as the ORM and Alembic for database migrations.
- **Dunning Scheduler**: Implemented as an independent cron process decoupled from the main web server to ensure that heavy scheduling operations do not block web request traffic.
- **Templating**: Utilizes Jinja2 for generating hosted portal views.
- **Testing**: Fully tested using the pytest framework.

## How to Run It

To run the application, ensure you have Docker installed:
1. Build and run the application containers using Docker.
2. The main web server runs on Uvicorn to handle API requests and webhook dispatching.
3. The independent cron process must be started to run the decoupled dunning scheduler.
4. Tests can be executed using pytest.