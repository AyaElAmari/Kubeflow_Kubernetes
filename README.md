# Orchestrating an ML Spark Pipeline with Kubeflow on Kubernetes

## Overall Project Architecture

![Project Architecture](https://github.com/AyaElAmari/Kubeflow_Kubernetes/blob/main/Architecture_kubefiw_kubernetes.png)

Provide a brief description of the architecture and key components of your project.

#
To run this project, you need to use the following command:

## Docker Installation
```bash
# official link to install Docker
https://www.docker.com/products/docker-desktop/
```

## Kubernetes installation
```bash
# Kubernetes installation command
your kubernetes command here

# official link to install minikube
https://kubernetes.io/fr/docs/setup/learning-environment/minikube/

# Launch Minikube command
minikube dashboard 

# Launch Kubernetes command
minikube dashboard 
```

## Kubeflow installation
```bash
# Kubeflow installation command
set PIPELINE_VERSION=2.0.5
kubectl apply -k "github.com/kubeflow/pipelines/manifests/kustomize/cluster-scoped-resources?ref=$PIPELINE_VERSION"
kubectl wait --for condition=established --timeout=60s crd/applications.app.k8s.io
kubectl apply -k "github.com/kubeflow/pipelines/manifests/kustomize/env/platform-agnostic-pns?ref=$PIPELINE_VERSION"

# Verify that the Kubeflow Pipelines UI is accessible by port-forwarding
kubectl port-forward -n kubeflow svc/ml-pipeline-ui 8080:80
```
