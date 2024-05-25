# Kubernetes_deploy_dog_cat_classifier
Deploy dog_cat classifier from Dockerhub to Kubernetes clusters (locally using Minikube)

## Getting Started

### Prerequisites

Before you begin, make sure you have [Docker](https://docs.docker.com/get-docker/) installed on your machine also install [Minikube] (https://minikube.sigs.k8s.io/docs/start/)

### Building Kubernetes cluster:
1. Start Minikube:
    ```bash
    minikube start
    ```
2. Check Minikube status if all clusters are running:
    ```bash
    minikube status
    ```
3. Apply yaml file config for deploy and service:
    ```bash
    kubectl -f dogcatapp.yaml
    ```
4. Check the status if all pods and services are running:
   ```bash
    kubectl get all
    ```
5. Run to access dog_cat app
    ```bash
    kubectl port-forward service/dogcat-service 19000:9000
    ```
6. Test with the added images of dog and cat / or own image
    - cat.jpg
    - dog.jpg