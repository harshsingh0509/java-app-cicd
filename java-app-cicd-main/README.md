# CI/CD Pipeline for Spring Boot Application using Maven, SonarQube, ArgoCD, Kubernetes and Docker

![image](https://github.com/RachanaVenkat/java-app-cicd/assets/151712438/df08e8f3-a2e1-4c0b-b99c-588801983055)

## Introduction

This CI/CD pipeline provides an automated method for building, testing, and deploying a Spring Boot application using Jenkins, SonarQube, Docker, and Argo CD. This pipeline integrates continuous integration practices into continuous delivery and deployment, thus providing good development workflow.

## Steps of the Pipeline

### Continuous Integration

1. **Step 1 - Check Out Code from SCM**:
   - Pull the source code from the repository.

2. **Step 2 - Trigger Jenkins Pipeline**: 
   - GitHub webhook configuration or repository path provided in the Jenkins.

3. **Step 3 - Build Java Application Using Maven**: 
   - Use Maven targets to build an application on a Docker image.

4. **Step 4 - Static Code Analysis with SonarQube**: 
   - Perform static code analysis, code scans, and vulnerability checks using SonarQube.

5. **Step 5 - Build and Push Docker Image**:
   - Build the docker image and push into a Docker registry.

### End of Continuous Integration

### Continuous Delivery/Deployment

1. **Step 6 - Monitor Docker Image**:
   - Monitor the docker image for changes with shell scripts or Argo Image Updater.

2. **Step 7 - Update Manifests Repository**: 
   - Update the deployment configurations in the `deployment.yml`.

3. **Step 8 - Argo CD Deployment**:
   - Synchronize the Manifest repository into the Kubernetes cluster.

4. **Step 9 - Deploy Application on Kubernetes**: 
   - Deploy application and verify running on the desired number of pods.
