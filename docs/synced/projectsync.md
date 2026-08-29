---
title: ProjectSync
stack: [Python, FastAPI, Google ADK, Google GenAI, Gemini 3.5, Pydantic, Google Cloud Firestore, PyGithub, React, TypeScript, Vite, Docker, Google Cloud Run]
date: October 2023
---

## What the project does
ProjectSync automates the process of creating documentation, portfolio entries, resume bullets, and social posts from finished GitHub repositories. It turns shipped code into career assets in one click.

## How it is built
The application is built as a 7-node Directed Acyclic Graph (DAG) workflow using Google ADK 2.0, which combines deterministic Python nodes and agentic nodes. The backend is powered by FastAPI and Google Cloud Firestore, deployed on Google Cloud Run, and serves a Vite-built React frontend directly. It features a zero-temperature evaluator quality gate, a human-in-the-loop approval workflow with Firestore persistence, an adaptive style memory curator that learns from user edits, and automatic commits of approved assets to a portfolio repository using PyGithub.

## How to run it
The application is containerized with Docker and can be deployed to Google Cloud Run. The backend is powered by FastAPI, which directly serves the React single-page application built with Vite. Note that the repository scan does not show any CI/CD workflow configuration files, such as GitHub Actions.