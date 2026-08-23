---
title: Crucible
stack:
  - React
  - TypeScript
  - Vite
  - FastAPI
  - Uvicorn
  - SQLite
  - Pydantic
  - Google Gemini API
  - React Flow
  - Framer Motion
  - Tailwind CSS
date: 2024-10-24
---

# Crucible

## What the Project Does
Crucible is an AI-powered idea workspace that visualizes reasoning as a structured node graph alongside a chat interface. It eliminates conversation drift and coherence loss in long AI chats by externalizing the AI's reasoning in real time onto an interactive node graph.

Key features include:
- **Spotlight Capture**: Input bar for quick idea entry.
- **Bubble Canvas**: Interactive node graph mapping claims, users, assumptions, and scope.
- **Contradiction Engine**: Real-time semantic checking of requests against assumptions.
- **Traceable Roadmap**: Transitions the canvas into a step-by-step execution plan.
- **Human-in-the-loop Go/No-Go**: Verdict options highlighting riskiest assumptions.
- **Web Search Grounding**: Grounding using Gemini's search grounding tool.

## How It Is Built
Crucible uses a split-pane architecture:
- **Frontend**: Built with React, TypeScript, Vite, and React Flow for rendering the interactive node canvas. Framer Motion and Tailwind CSS are used for styling and animations.
- **Backend**: Powered by FastAPI, which handles session persistence in SQLite and communicates with the Google Gemini API to generate chat responses, canvas updates, and execution plans. Pydantic is used for data validation.
- **Communication**: Uses Server-Sent Events (SSE) to stream chat tokens and canvas updates simultaneously between the frontend and backend.

## How to Run It
To run Crucible, you must configure and run both components of the application:
1. Start the backend server with FastAPI and Uvicorn.
2. Start the frontend development server using Vite.