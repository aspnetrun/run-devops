# Deploying .Net Microservices to Azure Kubernetes Services(AKS) and Automating with Azure DevOps
Deploying .Net Microservices into Kubernetes, and moving deployments to the cloud Azure Kubernetes Services (AKS) with using Azure Container Registry (ACR) and how to Automating Deployments with Azure DevOps and GitHub.

| Image | Status |
| ------------- | ------------- |
| Shopping Client |  [![Build Status](https://dev.azure.com/ezozkme/shopping/_apis/build/status/shoppingclient-pipeline?branchName=main)](https://dev.azure.com/ezozkme/shopping/_build/latest?definitionId=14&branchName=main) |
| Shopping API | [![Build Status](https://dev.azure.com/ezozkme/shopping/_apis/build/status/shoppingapi-pipeline?branchName=main)](https://dev.azure.com/ezozkme/shopping/_build/latest?definitionId=13&branchName=main) | | |


**UDEMY COURSE WITH DISCOUNTED - Step by Step Development of this repository -> https://www.udemy.com/course/deploying-net-microservices-with-k8s-aks-and-azure-devops/?couponCode=SEPT23**

**Check Explanation of this Repository on Medium -> https://mehmetozkaya.medium.com/deploying-net-microservices-to-azure-kubernetes-services-aks-and-automating-with-azure-devops-c50bdd51b702**

### Overall Picture
See the overall picture. You can see that we will have 3 microservices which we are going to develop and deploy together.

![Overall Picture of Repository](https://user-images.githubusercontent.com/1147445/105671396-b152f580-5ef3-11eb-8f3b-7f9f7c9c4d24.png)

### Shopping MVC Client Application
First of all, we are going to develop Shopping MVC Client Application For Consuming Api Resource which will be the Shopping.Client Asp.Net MVC Web Project. But we will start with developing this project as a standalone Web application which includes own data inside it. And we will add container support with DockerFile, push docker images to Docker hub and see the deployment options like “Azure Web App for Container” resources for 1 web application.
### Shopping API Application
After that we are going to develop Shopping.API Microservice with MongoDb and Compose All Docker Containers.
This API project will have Products data and performs CRUD operations with exposing api methods for consuming from Shopping Client project.
We will containerize API application with creating dockerfile and push images to Azure Container Registry.
### Mongo Db
Our API project will manage product records stored in a no-sql mongodb database as described in the picture.
we will pull mongodb docker image from docker hub and create connection with our API project.
At the end of the section, we will have 3 microservices whichs are Shopping.Client — Shopping.API — MongoDb microservices.
As you can see that, we have
* Created docker images,
Compose docker containers and tested them,
Deploy these docker container images on local Kubernetes clusters,
Push our image to ACR,
Shifting deployment to the cloud Azure Kubernetes Services (AKS),
Update microservices with zero-downtime deployments.
### Deploy to Azure Kubernetes Services (AKS) through CI/CD Azure Pipelines
And the last step, we are focusing on automation deployments with creating CI/CD pipelines on Azure Devops tool. We will develop separate microservices deployment pipeline yamls with using Azure Pipelines.
When we push code to Github, microservices pipeline triggers, build docker images and push the ACR, deploy to Azure Kubernetes services with zero-downtime deployments.

![cicd](https://user-images.githubusercontent.com/1147445/105671542-f37c3700-5ef3-11eb-9532-59a5855214d0.png)

You’ll see how to deploy your multi-container microservices applications with automating all deployment process seperately.
