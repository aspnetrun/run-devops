# Deploying .Net Microservices to Azure Kubernetes Services(AKS) and Automating with Azure DevOps
Deploying .Net Microservices into Kubernetes, and moving deployments to the cloud Azure Kubernetes Services (AKS) with using Azure Container Registry (ACR) and last section is we will learn how to Automating Deployments with Azure DevOps and GitHub.

[![Build Status](https://dev.azure.com/ezozkme/shopping/_apis/build/status/shoppingclient-pipeline?branchName=main)](https://dev.azure.com/ezozkme/shopping/_build/latest?definitionId=14&branchName=main)

[![Build Status](https://dev.azure.com/ezozkme/shopping/_apis/build/status/shoppingapi-pipeline?branchName=main)](https://dev.azure.com/ezozkme/shopping/_build/latest?definitionId=13&branchName=main)

UDEMY COURSE WITH DISCOUNTED - Step by Step Development of this repository -> https://www.udemy.com/course/using-grpc-in-microservices-communication-with-net-5/?couponCode=148712949BFD61FA9D78

**Check Explanation of this Repository on Medium -> https://mehmetozkaya.medium.com/deploying-net-microservices-to-azure-kubernetes-services-aks-and-automating-with-azure-devops-c50bdd51b702**

### Overall Picture
See the overall picture. You can see that we will have 3 microservices which we are going to develop and deploy together.

![Overall Picture of Repository](https://user-images.githubusercontent.com/1147445/98652230-5f66ee80-234c-11eb-9201-8b291b331c9f.png)

Basically we will implement e-commerce logic with only gRPC communication. We will have 3 gRPC server applications which are Product — ShoppingCart and Discount gRPC services. And we will have 2 worker services which are Product and ShoppingCart Worker Service. Worker services will be client and perform operations over the gRPC server applications. And we will secure the gRPC services with standalone Identity Server microservices with OAuth 2.0 and JWT token.

### ProductGrpc Server Application
First of all, we are going to develop ProductGrpc project. This will be Asp.Net gRPC Server Web Application and expose apis for Product CRUD operations.
