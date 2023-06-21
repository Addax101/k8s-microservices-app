# k8s-microservices-app
This repository contains the code for a cloud-native application developed using a *microservices architecture* and container orchestration with Kubernetes.

## Architural Diagram 
```mermaid
graph LR
  A[Kubernetes Cluster] -- Ingress --> B(Service1: Go)
  A -- Ingress --> C(Service2: Python)
  A -- Ingress --> D(Service3: JavaScript)
  B -- Service-to-Service --> C
  C -- Service-to-Service --> D

## Getting Started
These instructions will get you a copy of the project up and running on your local machine for development and testing purposes.

## Prerequisites
* Docker
* Kubernetes
* kubectl
* Helm
* Skaffold (optional)
## Installing
* Clone the repository git clone https://github.com/Addax101/k8s-microservices-app.git
* Build the Docker images for the microservices
`cd k8s-microservices-app`
`docker build -t service1:latest service1/`
`docker build -t service2:latest service2/`
* Deploy the application to a Kubernetes cluster using Helm `helm install --name my-release charts/`
* Use kubectl to check the status of the pods and services
`kubectl get pods`
`kubectl get services`
## Optional: Continuous Development with Skaffold
If you want to use Skaffold for continuous development, you can use the following command to build, deploy, and watch for changes in the code: `skaffold dev`
## Built With
* Docker - Containerization
* Kubernetes - Container orchestration
* Helm - Package manager for Kubernetes
## Authors

## License
This project is licensed under the MIT License - see the LICENSE.md file for details.

## Acknowledgments
GPS (Check out her awesome Youtube channel)
