# CI/CD Pipeline for Java application, using Maven, SonarQube, Argo CD, Docker and Kubernetes

![228301952-abc02ca2-9942-4a67-8293-f76647b6f9d8](https://github.com/user-attachments/assets/220a8a86-c3d3-4a44-b87e-814b2da8ee34)


This CI/CD pipeline provides an automated method for building, testing, and deploying a Spring Boot application using Jenkins, SonarQube, Docker, and Argo CD. This pipeline integrates continuous integration practices into continuous delivery and deployment, thus providing good development workflow.

## Steps of the Pipeline

### Continuous Integration

**Step 1 - Check Out Code from SCM**:
   - Pull the source code from the repository.

**Step 2 - Trigger Jenkins Pipeline**: 
   - GitHub webhook configuration or repository path provided in the Jenkins.

**Step 3 - Build Java Application Using Maven**: 
   - Use Maven targets to build an application on a Docker image.

**Step 4 - Static Code Analysis with SonarQube**: 
   - Perform static code analysis, code scans, and vulnerability checks using SonarQube.

**Step 5 - Build and Push Docker Image**:
   - Build the docker image and push into a Docker registry.

### End of Continuous Integration

### Continuous Delivery/Deployment

**Step 6 - Argo CD Deployment**:
   - Synchronize the Manifest repository into the Kubernetes cluster.

**Step 7 - Deploy Application on Kubernetes**: 
   - Deploy application and verify running on the desired number of pods.
     

