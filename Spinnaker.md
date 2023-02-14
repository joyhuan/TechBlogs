# Spinnaker
Spinnaker is an **open source**, **multi-cloud continuous delivery** platform for **releasing** software changes with high velocity and confidence.

Cloud Native Continuous Delivery
Fast, safe, repeatable deployments for every enterprise

## Spinnaker provides two core sets of features:

- Application management

- Application deployment

In addition, Spinnaker provides a higher-level experience that builds on top of the above features via Managed delivery.

### Application management

view and manage cloud resources

Modern tech organizations operate collections of services -- sometimes referred to as "applications" or "microservices."

**Applications, clusters**, and **server groups** are the key concepts Spinnaker uses to describe your services.
**Load balancers and firewalls** describe how your services are exposed to users.

#### Application
An application in Spinnaker is a collection of clusters, which in turn are collections of server groups. The application also includes firewalls and load balancers.

An application represents the service which you are going to deploy using Spinnaker, all configuration for that service, and all the infrastructure on which it will run.

You will typically create a different application for each service, though Spinnaker does not enforce that.

#### Cluster
Logical groupings of Server Groups in Spinnaker.

#### Server Group 
The base resource, the Server Group, identifies the deployable artifact (VM image, Docker image, source location) and basic configuration settings such as number of instances, autoscaling policies, metadata, etc. This resource is optionally associated with a Load Balancer and a Firewall. When deployed, a Server Group is a collection of instances of the running software (VM instances, Kubernetes pods).

#### Load Balancer 
A Load Balancer is associated with an ingress protocol and port range. It balances traffic among instances in its Server Groups. Optionally, you can enable health checks for a load balancer, with flexibility to define health criteria and specify the health check endpoint.

#### Firewall 
A Firewall defines network traffic access. It is effectively a set of firewall rules defined by an IP range (CIDR) along with a communication protocol (e.g., TCP) and port range.

### Application deployment

#### Pipeline
The pipeline is the key deployment management construct in Spinnaker. It consists of a sequence of actions, known as stages. You can pass parameters from stage to stage along the pipeline.

#### Stage
A Stage in Spinnaker is a collection of sequential Tasks and composed Stages that describe a higher-level action the Pipeline will perform either linearly or in parallel.

#### Task
A Task in Spinnaker is an automatic function to perform.

#### Deployment strategies

### Managed delivery
Managed Delivery takes Spinnaker’s infrastructure management and deployment capabilities to a new level by abstracting away many of the low-level details of configuring infrastructure and delivery workflows, and focusing on your application requirements, specified in a declarative format.

It allows you to declare the desired state of your application in terms of logical environments (think test and prod) where your cloud infrastructure resources exist (e.g. compute clusters), and where your software artifacts (think Debian package or Docker image) are deployed. Spinnaker automatically detects when a new version of your code is available for deployment and satisfies any deployment constraints you may have configured, or when your infrastructure resources diverge from the desired state, and acts upon that information to reconcile the current with the desired state.

----------------------------------------------------------------------------------------------------------------------
## Key concepts
### Clusters
Spinnaker acts as a single pane of glass from which to manage your global deployments across multiple clouds. The Clusters section of the UI acts as command and control base where we can increasingly layer on information relevant to deploying your applications.

### Pipelines
Pipelines are the essential tool in Spinnaker for controlling how to deploy your application. A pipeline is composed of a series of stages that can be combined in almost any order, which makes pipelines flexible, consistent and repeatable.

### Providers
In Spinnaker, a Cloud Provider is an interface to a set of virtual resources over which Spinnaker has control.
