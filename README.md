# Argo Microservice Sample

This repository contains a sample structure for deploying a microservice to a Kubernetes cluster managed by ArgoCD.

## 📁 Directory Structure

argo-microservice-sample/
├── .gitignore
├── README.md
├── applicationset.yaml 
└── lab/
    └── my-service/
        ├── deployment.yaml
        └── service.yaml

## 🚀 Getting Started

1. Create a namespace:
    ```bash
    kubectl create namespace lab
    ```

2. Create a Docker Hub image pull secret:
    ```bash
    kubectl create secret docker-registry regcred \
      --docker-username=your-dockerhub-username \
      --docker-password=your-dockerhub-password \
      --docker-email=your-email@example.com \
      --namespace=lab
    ```

3. Apply the ArgoCD Application:
    ```bash
    kubectl apply -f application.yaml -n argocd
    ```

## 📄 File Descriptions

- **application.yaml** - ArgoCD application configuration
- **deployment.yaml** - Kubernetes deployment for your microservice
- **service.yaml** - Kubernetes service to expose the microservice

## 📝 License

MIT License
