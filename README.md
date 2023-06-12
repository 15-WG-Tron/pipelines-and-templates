# Tron CI Pipelines

This repository contains CI pipeline files for the Tron organization. These pipelines are designed to automate the continuous integration process and ensure code quality across Tron projects.

## Pipelines

### CI Pipeline

The CI pipeline is triggered on every commit to a branch. It performs the following stages:

- Load scripts, if needed
- Environment variable validation, if needed
- Build
- Unit tests
- Dependency installation
- Code linting
- Dependency check
- Fortify ScanCentral Scan
- SonarCloud Scan
- TruffleHog OSS Scan

### Deployment Pipeline

The deployment pipeline is triggered when changes are merged to the master branch. It includes the following stages:

- End-to-end tests
- Penetration testing
- Deploy to staging
- Manual control for deploying to production

## Workflow Files

The CI pipeline workflow files are organized in the `.github/workflows` directory of this repository. You can find the following files:

- `.github/workflows/commit-branch.yaml`: Defines the Commit Branch pipeline workflow.
- `.github/workflows/merge-to-master.yaml`: Defines the Merge to Master pipeline workflow.

## Usage

To use these CI pipelines in your Tron projects, you can include the appropriate workflow file in your project repository's `.github/workflows` directory. Adjust the file as needed based on your project's specific requirements.

Make sure to configure any necessary environment variables and adjust the steps to match your project's build, testing, and deployment processes.

## Contributing

We welcome contributions to enhance and improve the CI pipelines in this repository. If you have suggestions, bug fixes, or new features, please feel free to submit a pull request.

