# Kubernetes
## Dockerfile
- Descrives the build process for an image
- Can be run to automatically create an image
- Contains all the commands necessary to build the image and run your application

## Container Orchestration
Deploying and scaling containers

## Kubernetes Vocab
- Node
    - Kubelet
    - Communicates with master
    - Runs pods
- Pod
    - Runs 1+ containers
    - Exists on a node
- Service
    - Handles requests
    - Usually a load balancer
- Deployment
    - Defines desired state - kubernetes handles the rest