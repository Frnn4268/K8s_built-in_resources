# Kubernetes Resource Types

This repository provides hands-on examples for working with Kubernetes' built-in resource types, catering to diverse application deployment and operational needs.

## Overview

Each directory corresponds to a specific Kubernetes resource type and includes a `Taskfile` that outlines the commands required to create, interact with, and clean up the resource.  
Examples are deployed into unique namespaces to avoid naming conflicts and simplify cleanup, as deleting a namespace removes all associated resources.

## How to Use

1. Navigate to the directory for the resource type you want to explore.
2. Use the `Taskfile` to follow the step-by-step process:
   - Create a namespace for the resources:
     ```
     task 01-create-namespace
     ```
   - Run the other tasks in sequence to create and manage resources.
   - Finally, delete the namespace to clean up:
     ```
     task 07-delete-namespace
     ```

## Included Resource Types

The following Kubernetes resource types are covered in this repository:  

- **Namespace**: Organize cluster resources by dividing them between multiple users.  
- **Pod**: The smallest deployable unit, representing one or more containers running in the cluster.  
- **ReplicaSet**: Maintains a desired number of pod replicas to ensure application availability.  
- **Deployment**: Manages stateless applications with features like rolling updates and rollbacks.  
- **Service**: Defines a policy for accessing a group of pods as a single logical entity.  
- **Job**: Runs one or more pods until a task is completed.  
- **CronJob**: Schedules jobs to execute at specific times or intervals.  
- **DaemonSet**: Ensures that specific pods are running on all or selected nodes in the cluster.  
- **StatefulSet**: Manages stateful applications with guarantees around pod identity and ordering.  
- **ConfigMap**: Stores non-sensitive configuration data for consumption by pods.  
- **Secret**: Stores sensitive data like credentials, tokens, or keys securely.  
- **Ingress**: Manages external HTTP/HTTPS access to services within the cluster.  
- **GatewayAPI**: Handles advanced traffic routing and control within the cluster.  
- **PersistentVolume (PV) and PersistentVolumeClaim (PVC)**: Provides persistent storage for pods.  
- **RBAC (Role-Based Access Control)**: Configures permissions and access control within the cluster.

## Out of Scope

The following resource types are not covered in detail but may be explored later:  

- **LimitRange**: Sets constraints on resource usage within a namespace.  
- **NetworkPolicy**: Controls network traffic flow at the IP/port level.  
- **MutatingWebhookConfiguration**: Configures webhooks for modifying API server requests.  
- **ValidatingWebhookConfiguration**: Sets webhooks for validating API server requests.  
- **HorizontalPodAutoscaler**: Automatically adjusts pod counts based on metrics like CPU usage.  
- **CustomResourceDefinition (CRD)**: Allows the creation of custom resource types in Kubernetes.  

## Notes

- Follow the order of resource types as outlined in this README for a structured learning experience.  
- Each example aligns with best practices, making it easier to understand and apply in real-world scenarios.  

---

Explore and experiment with these Kubernetes resource types to deepen your understanding of managing workloads and configurations in Kubernetes!