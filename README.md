University Department Website — DevOps Project
Project Title

University Computer Science Department Website with CI/CD Pipeline using GitHub Actions, Docker, GitHub Environments, and Render

Project Overview

This project is a static university department website developed as part of a DevOps lab assignment. It demonstrates a complete end-to-end CI/CD pipeline using modern DevOps practices.

The system simulates a real-world deployment workflow where code moves through different environments before reaching production.

The website includes:

Home page
Courses page
Faculty page
Admissions page
Contact page

The application is containerized using Docker and deployed across multiple environments using Render.

Tech Stack
HTML5
CSS3
Docker
Git & GitHub
GitHub Actions (CI/CD)
GitHub Environments (Secrets Management)
Render (Deployment Platform)
Git Flow Strategy

The project follows Git Flow methodology:

develop branch is used for active development
staging branch is used for testing and QA
main branch is used for production deployment

Workflow:

Code is developed in the develop branch. After validation, it is merged into staging for testing. Once verified, it is merged into main for production release.

CI/CD Pipeline
Continuous Integration (CI)

CI is implemented using GitHub Actions.

On every push to develop, staging, or main:

HTML and CSS validation is performed
Docker image build is tested
Repository structure is verified

The workflow file is located at:
.github/workflows/ci.yml

Continuous Deployment (CD)

Deployment is fully automated using Render.

Each branch is connected to a separate deployment environment:

develop → Development environment
staging → QA / Testing environment
main → Production environment
GitHub Environments and Secrets

This project uses GitHub Environments as required by the assignment.

Three environments are configured:

development
staging
production

Each environment contains a secret:

RENDER_DEPLOY_HOOK

These secrets securely trigger deployments on Render without exposing sensitive URLs in the codebase.

Docker Implementation

The application is containerized using Docker.

The Dockerfile uses nginx:alpine as the base image and serves the static website through an Nginx web server.

This ensures consistent deployment across all environments.

DevOps Features Implemented
Git Flow branching strategy
Continuous Integration using GitHub Actions
Continuous Deployment using Render
Docker containerization
Multi-environment deployment (Dev, Staging, Production)
GitHub Environments for secret management
Automated deployment using deploy hooks
Architecture Overview

The workflow of this system is as follows:

Developer commits code to GitHub repository. GitHub Actions triggers the CI pipeline to validate and build the Docker image. If successful, the CD pipeline triggers deployment through Render using environment-specific deploy hooks. Each branch is deployed to its respective environment.

Key Learning Outcomes

This project demonstrates practical understanding of:

CI/CD pipelines
Git Flow methodology
Docker containerization
Multi-environment deployment strategy
Secure secret management using GitHub Environments
Cloud-based deployment automation
Conclusion

This project successfully implements a full DevOps pipeline from development to production. It demonstrates automation, scalability, and structured software delivery using modern DevOps tools and practices.