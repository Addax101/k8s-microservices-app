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




