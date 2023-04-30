# DevOps Task

This repository contains Dockerfiles, Helm charts, and a CI/CD pipeline for deploying a website's microservices to a Kubernetes cluster on Google Cloud Platform (GCP) using GitHub Actions.

## Prerequisites

1. A GCP project with a Kubernetes cluster and Google Container Registry (GCR) set up.
2. A GitHub repository containing the source code for your microservices.
3. Dockerfiles and Helm charts for each microservice.
4. A GCP Service Account with the necessary permissions to access and manage the Kubernetes cluster and GCR.

## Instructions

1. Add your GCP project ID, Kubernetes namespace, and Service Account key in JSON format as secrets to your GitHub repository. Name the secrets `GCP_PROJECT_ID`, `K8S_NAMESPACE`, and `GCP_SA_KEY`, respectively.

2. Update the `devops-task.github/workflows/pipelines.yml` file with the correct paths to your Dockerfiles, Helm charts, and GCR.

3. Push your changes to the `main` branch. The CI/CD pipeline will automatically build the Docker images, push them to GCR, and deploy the microservices to your Kubernetes cluster on GCP.

4. Monitor the progress of your GitHub Actions workflow by clicking the "Actions" tab in your GitHub repository.

## Customization

Update the environment variables and configurations in the `devops-task/.github/workflows/pipelines.yml` file, Dockerfiles, and Helm charts to match your specific microservices and infrastructure requirements.


