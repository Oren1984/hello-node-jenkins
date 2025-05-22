# Hello Node Jenkins Pipeline

This repository contains a simple Node.js application with a Jenkins pipeline configured to build, run, and test the app inside Docker containers.

---

## Project Structure

- `Dockerfile` - Defines the Node.js Docker image.
- `app.js` - A simple Node.js application that prints "Hello, World!".
- `package.json` - Node.js project metadata and dependencies.
- `Jenkinsfile` - Jenkins pipeline script with the following stages:
  - Code Checkout
  - Docker Build + Tag
  - Docker Run

---

## How to Use

### Prerequisites

- Docker installed and running
- Jenkins server running inside Docker
- Git installed

### Steps

1. Clone the repository:
   ```bash
   git clone https://github.com/oren1984/hello-node-jenkins.git
   cd hello-node-jenkins
