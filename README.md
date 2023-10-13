# k8s
Kubernetes learning project

Goal: from local development on sample app to k8s powered

# What is Kubernetes
K8s is a platform for managing application containers across multiple hosts. It abstracts away the underlying hardware infrastructure and acts as a distributed operating system for your cluster.
Also is as a platform for building other higher level platforms like OpenShift.

Plays 3 roles:

1.Referee
- allocates and manages resources (build-in absractions: Persistent Volume Claims, Resource Quotas, Services)
- provides control plane for scheduling, prioritizing, and running processes
- provides a sandboxed environment so that applications do not interfere with each other
- allows to specify resources (CPU, RAM) per application and ensures these limits
- provides communication mechanism so that services can talk among each other if required 

2.Illusionist
- gives the illusion of single infinite compute resource by abstracting away the hardware infrastructure
- provides the illusion that you need not care about underlying infrastructure (can run on a bare metal, in data centre, on the public cloud, or even hybrid cloud)
- gives the illusion that applications need not care about where they will be running

3.Glue
- provides common abstractions like Services, Ingress, auto scaling, rolling deployment , volume management
- comes with some security features: Namespaces, RBAC that applications can use transparently
