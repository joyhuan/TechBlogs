# Kubernetes
Production-Grade Container Orchestration

Kubernetes, also known as K8s, is an open-source system for automating deployment, scaling, and management of containerized applications.

## What can Kubernetes do for you
## Features
- Automated rollouts and rollbacks
- Storage orchestration
- Automatic bin packing
- IPv4/IPv6 dual-stack
- Self-healing
- Service discovery and load balancing
- Secret and configuration management
- Batch execution
- Horizontal scaling
- Designed for extensibility

## Dockerfile
- Describes the build process for an image
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