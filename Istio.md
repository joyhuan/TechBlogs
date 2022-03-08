# Istio

Simplify observability, traffic management, security, and policy with the leading service mesh.

Istio extends Kubernetes to establish a programmable, application-aware network using the powerful Envoy service proxy. Working with both Kubernetes and traditional workloads, Istio brings standard, universal traffic management, telemetry, and security to complex deployments.

## What is a Service Mesh?
A service mesh is a dedicated infrastructure layer that you can add to your applications. It allows you to transparently add capabilities like observability, traffic management, and security, without adding them to your own code. The term “service mesh” describes both the type of software you use to implement this pattern, and the security or network domain that is created when you use that software.

## How it Works
Istio has two components: the data plane and the control plane.

The data plane is the communication between services. Without a service mesh, the network doesn’t understand the traffic being sent over, and can’t make any decisions based on what type of traffic it is, or who it is from or to.

Service mesh uses a proxy to intercept all your network traffic, allowing a broad set of application-aware features based on configuration you set.

An Envoy proxy is deployed along with each service that you start in your cluster, or runs alongside services running on VMs.

The control plane takes your desired configuration, and its view of the services, and dynamically programs the proxy servers, updating them as the rules or the environment changes.

## Concepts
### Traffic management
Routing traffic, both within a single cluster and across clusters, affects performance and enables better deployment strategy. Istio’s traffic routing rules let you easily control the flow of traffic and API calls between services. Istio simplifies configuration of service-level properties like circuit breakers, timeouts, and retries, and makes it easy to set up important tasks like A/B testing, canary deployments, and staged rollouts with percentage-based traffic splits.

### Observability
As services grow in complexity, it becomes challenging to understand behavior and performance. Istio generates detailed telemetry for all communications within a service mesh. This telemetry provides observability of service behavior, empowering operators to troubleshoot, maintain, and optimize their applications. Even better, you get almost all of this instrumentation without requiring application changes. Through Istio, operators gain a thorough understanding of how monitored services are interacting.

Istio’s telemetry includes detailed metrics, distributed traces, and full access logs. With Istio, you get thorough and comprehensive service mesh observability.

### Security capabilities
Microservices have particular security needs, including protection against man-in-the-middle attacks, flexible access controls, auditing tools, and mutual TLS. Istio includes a comprehensive security solution to give operators the ability to address all of these issues. It provides strong identity, powerful policy, transparent TLS encryption, and authentication, authorization and audit (AAA) tools to protect your services and data.

Istio’s security model is based on security-by-default, aiming to provide in-depth defense to allow you to deploy security-minded applications even across distrusted networks.

## Solutions
Increasing Kubernetes deployment and management efficiency
