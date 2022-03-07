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

## Declarative Model
K8s utilizes infrastructure-as-code concepts. All resources and configurations are done in declarative YAML files called resource templates or manifests and applied to your cluster.

## KIND
Kubernetes in Docker (KIND) uses Docker containers as your Kubernetes nodes.

## Kubectl
Kubectl provides the command line interaction with your cluster. This is how 
you’ll view and manage things like pods, services, etc, and apply template files to your cluster. Kubectl is a REST API client to the kube-api-server.

## Contexts
Kubectl can be pointed to different clusters for management. If you installed 
minikube and also activated Kubernetes for Docker, you’ll need to tell 
kubectl which cluster to work on. You do this with context.

## A REST API
Kubernetes is an API-driven system. EVERY resource/object that exists in 
the system is a REST resource.

## Event-Driven
Kubernetes is an event driven system. This enables Kubernetes respond to 
changes extremely rapidly. 

## Core Components
- Master components - the controller for the cluster. Also known as the "control plane"
- Nodes - the servers in our cluster. There are master nodes and worker nodes.
- Workloads - running containers to do the work. These can be created in several ways as we'll see.
- Services - provide network connectivity to workloads.

## Master Components

