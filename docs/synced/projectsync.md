---
title: ProjectSync
stack: Python, FastAPI, React, TypeScript, Vite, Google ADK, Google GenAI, Pydantic, Google Cloud Firestore, Google Cloud Run, PyGithub, Docker
date: 2024-10-24
---

## What ProjectSync does
ProjectSync is an autonomous Taskmaster AI Agent that extracts technical architecture from finished GitHub repositories to generate multi-format career assets in one click. It converts shipped GitHub code into documentation, resume bullets, portfolio cards, and social announcements, adapting automatically to the developer's voice. 

## How it is built
ProjectSync is built with a React-based web frontend (Vite, TypeScript) and a FastAPI backend. The backend runs an agentic pipeline using Google ADK 2.0 and Google GenAI, structured as a 7-Node Directed Acyclic Graph (DAG). The architecture uses a dual-layer memory system containing Semantic Style Rules and an Episodic Transaction Ledger. It stores state and memory in Google Cloud Firestore and deploys as a stateless container on Google Cloud Run. Integrations include PyGithub for codebase access and Pydantic for data validation. Key features include an Adaptive Curator Agent for human-in-the-loop style learning, dual-commit and human approval callbacks, and cooperative cancellation and resumption of pipelines.

## How to run it
1. Package the backend using the Docker configuration.
2. Deploy the stateless container to Google Cloud Run.
3. Configure Google Cloud Firestore for state and memory storage.
4. Set up environment variables for Google GenAI, Google ADK, and PyGithub.
5. Run the React-based web frontend locally or deploy the build output to your hosting provider.