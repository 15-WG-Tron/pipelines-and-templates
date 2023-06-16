# Tron CI/CD Pipelines and Pull Request Template

This repository contains CI/CD pipeline files and a pull request template for Tron. These pipelines are designed to automate the continuous integration process and ensure code quality across Tron projects. The pull request template provides a standardized format for creating pull requests, guiding contributors to provide essential information such as a clear description of the changes, associated issue numbers, and any additional context required for efficient review and merging of the code.

## Pipelines

### Continuous Intergration (CI) Pipeline

The Continuous Intergration pipeline is triggered on every commit to a branch. It performs the following stages:

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

### Continuous Deployment (CD) Pipeline

The Continuous Deployment pipeline is triggered when changes are merged to the master branch. It includes the following stages:

- End-to-end tests
- Deploy to staging
- Manual control for deploying to production

## Workflow Files

The CI pipeline workflow files are organized in the `.github/workflows` directory of this repository. You can find the following files:

- `.github/workflows/ci.yaml`: Defines the CI pipeline workflow.
- `.github/workflows/deployment-pipeline.yaml`: Defines the deployment pipeline workflow.

## Pull Request Template

When creating a pull request, please use the provided pull request template to ensure all necessary information is provided and naming conventions are followed. The pull request template is located at [PULL_REQUEST_TEMPLATE.md](./.github/PULL_REQUEST_TEMPLATE.md).

To use the pull request template:

1. Go to the project repository's `.github` directory.
2. Create a file called `PULL_REQUEST_TEMPLATE.md`.
3. Copy the contents of the [Pull Request Template](./.github/PULL_REQUEST_TEMPLATE.md) into the `PULL_REQUEST_TEMPLATE.md` file.
4. Customize the template as needed, including the pull request description, related issues, and the checklist.
5. Save the `PULL_REQUEST_TEMPLATE.md` file.

## Usage

To use these CI pipelines in your Tron projects, you can include the appropriate workflow file in your project repository's `.github/workflows` directory. Adjust the file as needed based on your project's specific requirements.

Make sure to configure any necessary environment variables and adjust the steps to match your project's build, testing, and deployment processes.

## Contributing

We welcome contributions to enhance and improve the CI pipelines in this repository. If you have suggestions, bug fixes, or new features, please feel free to submit a pull request.

