In the modern software development landscape, Continuous Integration and Continuous Deployment (CI/CD) pipelines are essential for ensuring that code changes are automatically built, tested, and deployed to production environments in a consistent and reliable manner. This document provides a comprehensive guide to setting up a robust CI/CD pipeline using various tools hosted on AWS EC2 instances.

The process will cover everything from setting up the necessary infrastructure to deploying an application on an Amazon EKS (Elastic Kubernetes Service) cluster, assigning a custom domain, and monitoring the application to ensure its stability and performance.

The pipeline will incorporate several industry-standard tools:

AWS EC2: Creating virtual machines.
Jenkins: Automating the build, test, and deployment processes.
SonarQube: Static code analysis to ensure code quality.
Trivy: File scan and vulnerability scanning for Docker images.
Nexus Repository Manager: Managing artifacts.
Terraform: Infrastructure as code to create the EKS Cluster.
Docker: Containerization for consistency and portability.
Kubernetes: Container orchestration for deployment.
Prometheus and Grafana: Monitoring the pipeline and application performance.
By following this guide, you'll be able to set up a fully functional CI/CD pipeline that supports continuous delivery and helps maintain high standards for code quality and application performance.

