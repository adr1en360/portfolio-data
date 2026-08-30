---
title: ProjectSync
stack: Python, FastAPI, React, TypeScript, Vite, Google ADK, Google GenAI, Pydantic, Google Cloud Firestore, Google Cloud Run, PyGithub, Vitest, Pytest
date: 2023-10-27
---

# ProjectSync

An autonomous Taskmaster AI Agent that turns finished GitHub repositories into career assets in one click.

## What the Project Does

ProjectSync automates the extraction of technical architecture from codebases to generate multi-format career assets. It produces documentation, resume bullets, portfolio cards, and social announcements directly from finished GitHub repositories.

### Key Features
- **7-Node Directed Acyclic Graph (DAG) agent workflow** for structured processing.
- **Dual-layer memory architecture** utilizing Semantic Style Rules and an Episodic Transaction Ledger.
- **Adaptive style memory curator** to manage voice personalization.
- **Human-in-the-loop approval** with a dual-commit workflow.
- **Multi-format asset generation** including resume bullets, social drafts, and documentation.

## How it is Built

ProjectSync is built with a React frontend (using TypeScript and Vite) and a FastAPI backend in Python. The backend executes an agentic pipeline using Google ADK 2.0 with a 7-node DAG structure. State and memory storage are managed using Google Cloud Firestore, and the entire system runs statelessly on Google Cloud Run. Code quality is maintained using PyGithub, Vitest, and Pytest.

## How to Run It

1. Configure your environment variables for Google Cloud Firestore and Google GenAI.
2. Start the FastAPI backend server.
3. Run the React frontend using Vite.