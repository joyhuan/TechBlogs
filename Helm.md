# Helm

The package manager for Kubernetes

Helm helps you manage Kubernetes applications — Helm Charts help you define, install, and upgrade even the most complex Kubernetes application.

Charts are easy to create, version, share, and publish — so start using Helm and stop the copy-and-paste.

## Helm Charts
- Bundle of YAML Files
- Create your own Helm Charts with Helm
- Push them to Helm Repo
- Download and use exisitng ones

## Feature 1. Templating Engine
1. Define a common blue print
2. Dynamic values are replaced by placeholders

## Feature 2. Same Applications across different environments

## Feature 3. Release Management

## Helm Chart Structure
![Helm Chart Structure](https://github.com/joyhuan/TechBlogs/blob/master/images/HelmChartStructure.png)

`helm install <chartname>` Template files will be filled with the values from values.yaml

-------
Below are from Educative
## What Problem Does Helm Resolve?
Kubernetes is a container orchestration platform that helps to deploy and manage software in a cloud. It helps to manage containerized applications (tools like Docker) by scaling them up and making sure that they’re available. Also, it takes over the burden of managing server infrastructure by providing an elegant abstraction.

These elegant abstractions are called Kubernetes objects and are represented in the .yaml files.
 
Pod represents a running application that usually consists of a single container (e.g., Docker). 

Although it’s possible to operate on Pod, it’s not recommended. Instead, we can use Deployment, which will not only create a Pod but also take care of several application instances. With Deployment, we can specify how many Pods we would like to have. If a container stops (due to an error in the program), Kubernetes will automatically start a new one to make sure that the number of running Pods is the same as what was set.

A minimal application setup would require defining one more thing—Service. Kubernetes API is built using the Unix philosophy that each object is designed to do one thing. As already mentioned, Pods are for wrapping one or more containers and Deployments are for managing their lifecycle. Services, on the other hand, have a different purpose.

They are designed to expose applications to other software either within or outside the Kubernetes cluster. 

Apart from Deployments and Services, applications installed on Kubernetes require other types of objects, such as the following:

Ingress: These are for managing external access to applications in a cluster.
Volumes: These represent a directory in which files and data can persist.
ConfigMap: This is used to store and inject environment variables to Pods.
Secret: This is similar to a ConfigMap, but it’s used for more sensitive information like passwords.
Custom resource: This is used to extend Kubernetes API and provide an infinite number of Kubernetes objects



## Core Concepts of Helm

### What is Helm?
Kubernetes package manager

“Helm is the best way to find, share, and use software built for Kubernetes.”

In Helm, a package is called a chart.

template — blueprints for all Kubernetes resource files

`helm install nginx-app ./nginx-chart --values ./values.yaml`

A release is a version of all Kubernetes resources that are running together in a cluster and are the outcome of a single helm install or helm upgrade command. 

### Key benefits of Helm
- Parameterized Kubernetes YAMLs: It enables the creation of a blueprint for Kubernetes resource files which can be reused across many applications to reduce the maintenance burden.
- Reduces the complexity of installing an application on Kubernetes: It can be achieved using a single command.
- Easy configuration of applications: Helm chart developers provide a high-level abstraction that makes it easy to work with the chart without knowing about the  Kubernetes API.
- Keeps track of the history of revisions: We can roll back to the state at any point in time.
- Enables testing of Kubernetes resources: Helm provides an easy-to-use testing and linting command that makes sure that all Kubernetes YAML files are written in high quality.
- Provides out-of-the-box Kubernetes solutions for many popular open-source solutions: Many Helm charts are available for free on Artifact Hub, so there is no need to build many solutions from scratch.