# heathermayhowse — Basic Jenkins Pipeline

A minimal CI pipeline exercise: a React app built and tested automatically through Jenkins.

## Overview

This repo is the starting point in a broader progression of CI/CD pipeline projects — see [Related Pipelines](#related-pipelines) below. The React app itself is a minimal starter template; the focus is the **Jenkinsfile**, establishing the foundational install → build → test pipeline that later projects build on.

## Pipeline Stages

1. **Build** — installs dependencies and creates the production build (`npm install && npm run build`)
2. **Test** — runs the test suite in CI mode (`npm test -- --watchAll=false`)

## Tech Stack

- **React** (Create React App)
- **Jenkins** (declarative pipeline, using a configured Node 20 tool)

## Getting Started

### Run the app locally
```bash
npm install
npm start
```
Visit [http://localhost:3000](http://localhost:3000).

### Run the pipeline
This pipeline is designed to run inside Jenkins with a Jenkins-configured Node.js tool (`Node20`).

## Related Pipelines

This repo is part of a progression through CI/CD concepts, each adding a new capability:

1. **`heathermayhowse`** (this repo) — basic pipeline: install → build → test
2. **`cicd-assignment2`** — adds automated deployment to Netlify
3. **`ci-demo`** — adds a Dockerized build stage and deployment to AWS S3
4. **`enterprise-computing-project`** — full pipeline: multi-stage Docker build (Nginx-served), push to AWS ECR, and deploy to ECS
