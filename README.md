# Pipelines

This repository contains my project's source code and is integrated with GitHub Actions for continuous integration and deployment.

## Pipelines

### CI Pipeline

The CI (Continuous Integration) pipeline runs on every commit to ensure code quality, run tests, and perform security checks. It consists of the following stages:

- Load scripts, if needed
- Environment variable validation, if needed
- Build
- Unit tests
- Dependency Installation
- Code linting
- Dependency check
- Fortify ScanCentral Scan
- SonarCloud Scan
- TruffleHog OSS Scan

### Deployment Pipeline

The deployment pipeline runs on merging changes to the main branch. It handles deploying the application to staging and provides manual control for deploying to production. The stages in this pipeline include:

- End-to-end tests
- Deploy to staging
- Manual control for deploying to production

## Workflow Files

- `.github/workflows/ci-pipeline.yaml`: Defines the CI pipeline workflow.
- `.github/workflows/deployment-pipeline.yaml`: Defines the deployment pipeline workflow.

## Usage

To run the pipelines manually or view their status, navigate to the "Actions" tab above and select the desired workflow.


