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

# ProjectSync

## What It Does
ProjectSync is an autonomous Taskmaster AI Agent that turns shipped GitHub repositories into career-ready assets with one click. It automates the extraction of technical architecture from finished codebases to generate multi-format career assets like documentation, resume bullets, portfolio cards, and social announcements.

### Key Features
* **7-Node Directed Acyclic Graph (DAG) Agent Workflow**: Engineered with Google ADK 2.0 to orchestrate plain Python nodes and AI agent nodes.
* **Dual-Layer Memory Architecture**: Features Semantic Style Rules and an Episodic Transaction Ledger.
* **Adaptive Curator Agent**: Learns and adapts to the developer's voice.
* **Human-in-the-Loop Approval**: Supports asset regeneration and dual-commit capabilities.
* **Multi-Platform Management**: Provides social drafts management and resume bullet bank CRUD operations.

## How It Is Built
ProjectSync is built with a decoupled architecture consisting of a React-based frontend and a FastAPI backend. The backend runs on Google Cloud Run and utilizes Google Cloud Firestore for state and memory storage. The core agent pipeline is structured as a 7-node DAG using Google ADK 2.0, combining plain Python nodes and AI agent nodes to ingest repositories, extract architecture, and generate career assets.

## How to Run It
### Prerequisites
* Python 3.10+
* Node.js and npm
* Google Cloud Platform account with Firestore and Cloud Run enabled

### Backend Setup
1. Navigate to the backend directory.
2. Install dependencies using pip.
3. Configure environment variables for Google GenAI, Google ADK, and Firestore.
4. Run the FastAPI application.

### Frontend Setup
1. Navigate to the frontend directory.
2. Install dependencies using npm.
3. Start the Vite development server.