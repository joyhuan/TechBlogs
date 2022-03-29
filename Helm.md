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
