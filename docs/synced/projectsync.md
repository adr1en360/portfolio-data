---
title: ProjectSync
stack:
  - Python
  - FastAPI
  - React
  - TypeScript
  - Vite
  - Google ADK
  - Google GenAI
  - Pydantic
  - Google Cloud Firestore
  - Google Cloud Run
  - PyGithub
  - Vitest
  - Pytest
date: 2023-10-27
---

## What the project does
ProjectSync is an autonomous Taskmaster AI Agent that extracts technical architecture details from GitHub repositories to generate multi-format career assets in a single click. It automates the creation of documentation, resume bullets, portfolio cards, and social announcements.

## How it is built
The system is built with a React frontend powered by TypeScript and Vite, and a backend running FastAPI. The backend executes an agentic pipeline using Google ADK 2.0 designed as a 7-node Directed Acyclic Graph (DAG) workflow. 

Key components include:
- Dual-layer memory architecture featuring Semantic Style Rules and an Episodic Transaction Ledger.
- Adaptive Curator Agent to facilitate human-in-the-loop style adaptation.
- Dual-commit and human approval callbacks.
- Cooperative cancellation and pipeline resumption.
- Storage management via Google Cloud Firestore, configured for stateless deployment on Google Cloud Run.
- Repository parsing utilizing PyGithub.

## How to run it
To run the backend, configure your FastAPI environment and execute the application to start the Google ADK 2.0 7-node DAG pipeline. Use Pytest to run backend tests. To run the frontend, navigate to the React directory, install the required dependencies, and launch the Vite development server. Use Vitest to execute frontend tests.