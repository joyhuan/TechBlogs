# Spinnaker
Spinnaker is an open source, multi-cloud continuous delivery platform for releasing software changes with high velocity and confidence.

Cloud Native Continuous Delivery
Fast, safe, repeatable deployments for every enterprise

## Spinnaker provides two core sets of features:

- Application management

- Application deployment

In addition, Spinnaker provides a higher-level experience that builds on top of the above features via Managed delivery.

### Application
An application in Spinnaker is a collection of clusters, which in turn are collections of server groups. The application also includes firewalls and load balancers.

An application represents the service which you are going to deploy using Spinnaker, all configuration for that service, and all the infrastructure on which it will run.

You will typically create a different application for each service, though Spinnaker does not enforce that.

### Cluster
Logical groupings of Server Groups in Spinnaker.

### Server Group 
The base resource, the Server Group, identifies the deployable artifact (VM image, Docker image, source location) and basic configuration settings such as number of instances, autoscaling policies, metadata, etc. This resource is optionally associated with a Load Balancer and a Firewall. When deployed, a Server Group is a collection of instances of the running software (VM instances, Kubernetes pods).

### Load Balancer 
A Load Balancer is associated with an ingress protocol and port range. It balances traffic among instances in its Server Groups. Optionally, you can enable health checks for a load balancer, with flexibility to define health criteria and specify the health check endpoint.

### Firewall 
A Firewall defines network traffic access. It is effectively a set of firewall rules defined by an IP range (CIDR) along with a communication protocol (e.g., TCP) and port range.

### Pipeline
The pipeline is the key deployment management construct in Spinnaker. It consists of a sequence of actions, known as stages. You can pass parameters from stage to stage along the pipeline.

### Stage
A Stage in Spinnaker is a collection of sequential Tasks and composed Stages that describe a higher-level action the Pipeline will perform either linearly or in parallel.

### Task
A Task in Spinnaker is an automatic function to perform.

