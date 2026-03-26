# CI/CD Pipeline for Containerized 2048 Game

![Architecture Diagram Placeholder](images/architecture-diagram.png)

## Overview
This project demonstrates a fully automated CI/CD pipeline for deploying a Dockerized version of the 2048 game using AWS. The pipeline builds, tests, and deploys the application to ECS Fargate, reducing manual intervention and ensuring consistent, scalable releases. It showcases best practices for DevOps, containerization, and serverless deployment.

## Problem Statement
Manual deployment of containerized applications is error-prone, slow, and difficult to scale. Without automation, updates require repetitive manual steps that can introduce configuration errors, downtime, and inconsistent environments. The challenge was to create a reliable pipeline that automates builds, image registry management, and production deployment securely.

## Solution
- AWS CodePipeline orchestrates the pipeline stages (build, test, deploy).  
- CodeBuild builds Docker images of the 2048 game and pushes them to Amazon ECR.  
- ECS Fargate deploys containers serverlessly, removing the need to manage EC2 instances.  
- IAM Roles enforce secure access between services.  
- The result is a fully automated, repeatable, and scalable CI/CD workflow.

![Workflow / Implementation Placeholder](images/workflow.png)

## Steps to be Performed 👩‍💻
1. Set Up ECS Cluster and ECR Repository  
2. Prepare the 2048 Game Code  
3. Configure CodeBuild for Continuous Integration  
4. Configure CodePipeline for Continuous Deployment  

## Key Services / Tools Used 🛠
- AWS CodePipeline: Orchestrates build and deploy stages [Automation]  
- AWS CodeBuild: Builds Docker images [Build]  
- Amazon ECR: Stores Docker images [Container Registry]  
- Amazon ECS (Fargate): Deploys containers [Deployment]  
- IAM Roles & Policies: Secure access across services [Security]  

## Results
![Application Screenshot Placeholder](images/results.png)  

## Future Improvements
- Add automated unit and integration tests in the pipeline  
- Monitor deployments using CloudWatch and notifications  
- Expand pipeline to support multiple environments (dev/staging/prod)  
