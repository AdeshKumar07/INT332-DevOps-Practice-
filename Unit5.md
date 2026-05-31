# Unit V: Continuous Integration (CI) with GitHub Actions

## 1. Understanding Workflow Automation
Automating tasks based on GitHub events.

## 2. Key Components
*   **Workflows:** The overall automated process.
*   **Events/Triggers:** What starts the workflow (`push`, `pull_request`, `schedule`).
*   **Jobs:** A set of steps that run on the same runner.
*   **Steps:** Individual tasks (e.g., running a script or an action).
*   **Actions:** Standalone commands.
*   **Runners:** The server that runs the jobs.

## 3. Job Strategies
*   **Matrix strategies:** Running jobs against multiple versions of a language/OS.
*   **Multi-job workflows:** Managing dependencies between jobs.

## 4. Optimization
*   **Marketplace actions:** Using pre-built community actions.
*   **Caching:** Faster builds by storing dependencies.

---

## Unit V Practical Commands

### Example Workflow (`.github/workflows/main.yml`)
```yaml
name: Docker CI

on:
  push:
    branches: [ "main" ]

jobs:
  build:
    runs-on: ubuntu-latest
    steps:
    - uses: actions/checkout@v3
    - name: Build Docker image
      run: docker build . -t my-app:${{ github.sha }}
    - name: Log in to Docker Hub
      run: echo "${{ secrets.DOCKER_PASSWORD }}" | docker login -u "${{ secrets.DOCKER_USERNAME }}" --password-stdin
    - name: Push image
      run: docker push my-app:${{ github.sha }}
```
