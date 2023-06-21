# k8s-microservices-app
This repository contains the code for a cloud-native application developed using a *microservices architecture* and container orchestration with Kubernetes.

## Architural Diagram 
```mermaid
flowchart LR

subgraph "Kubernetes Cluster"
  participant Node1
  participant Node2
  participant Node3
end

subgraph "Microservice A"
  participant ServiceA1
  participant ServiceA2
end

subgraph "Microservice B"
  participant ServiceB1
  participant ServiceB2
end

subgraph "Microservice C"
  participant ServiceC1
  participant ServiceC2
end

subgraph "Load Balancer"
  participant Ingress
end

Node1 --> ServiceA1
Node2 --> ServiceB1
Node3 --> ServiceC1

ServiceA1 --> ServiceA2
ServiceB1 --> ServiceB2
ServiceC1 --> ServiceC2

ServiceA2 --> Ingress
ServiceB2 --> Ingress
ServiceC2 --> Ingress
```



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
