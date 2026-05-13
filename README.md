University Department Website — DevOps Project
Project Title

University Computer Science Department Website with CI/CD Pipeline using GitHub Actions, Docker, and Render

Project Overview

This project is a static university department website developed as part of a DevOps lab assignment. It demonstrates a complete CI/CD pipeline using modern DevOps tools and practices.

The website provides information about the computer science department, including an overview page, courses offered, faculty information, admission guidelines, and contact details.

The application is containerized using Docker and deployed across multiple environments using Render.

Tech Stack

The project is built using HTML, CSS, Docker, Git, GitHub, GitHub Actions, and Render.

Git Flow Strategy

This project follows the Git Flow branching model.

The main branch is used for production-ready code. The staging branch is used for testing and quality assurance. The develop branch is used for active development and feature integration.

The workflow follows this pattern:

Feature development is done in the develop branch. Once stable, changes are moved to the staging branch for testing. After verification, code is merged into the main branch for production deployment.

CI/CD Pipeline Overview

Continuous Integration is implemented using GitHub Actions.

On every push to develop, staging, or main branches, the pipeline runs automated checks including HTML and CSS validation, Docker image build verification, and code structure validation.

The workflow file is located in .github/workflows/ci.yml.

Continuous Deployment is handled using Render. Each branch is automatically deployed to a separate environment.

The develop branch is deployed to the development environment. The staging branch is deployed to the QA or testing environment. The main branch is deployed to the production environment.

Docker Implementation

The project is containerized using Docker to ensure consistent execution across all environments.

The Dockerfile uses the nginx:alpine base image. It copies all project files into the nginx web directory and exposes port 80 to serve the static website.

Docker ensures that the application runs consistently regardless of the environment.

Live Deployment URLs

Development environment URL: replace-with-your-dev-url
Staging environment URL: replace-with-your-staging-url
Production environment URL: replace-with-your-production-url

(Replace these placeholders with your actual Render deployment links)

DevOps Features Implemented

This project includes Git Flow branching, continuous integration using GitHub Actions, Docker containerization, multi-environment deployment, automated deployment using Render, and branch protection rules for maintaining code quality and stability.

Architecture Overview

The workflow of the system starts from the developer pushing code to GitHub. GitHub Actions then runs the CI pipeline, which validates the code and builds the Docker image. After successful checks, Render pulls the code and deploys it to the appropriate environment based on the branch. This results in live deployment across development, staging, and production environments.

Key Learning Outcomes

This project demonstrates understanding of CI/CD pipelines, Git Flow methodology, Docker containerization, multi-environment deployment strategies, and automation of software delivery using cloud-based tools.
