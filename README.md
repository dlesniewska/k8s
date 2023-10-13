# k8s
Kubernetes learning project

Goal: from local development on sample app to k8s powered

# What is Kubernetes
K8s is a platform for **managing application containers across multiple hosts**. It abstracts away the underlying hardware infrastructure and acts as a **distributed operating system for your cluster**.
Also is as a platform for building other higher level platforms like OpenShift.

**Roles:**

**1.Referee**
- allocates and manages resources (build-in absractions: Persistent Volume Claims, Resource Quotas, Services)
- provides control plane for scheduling, prioritizing, and running processes
- provides a sandboxed environment so that applications do not interfere with each other
- allows to specify resources (CPU, RAM) per application and ensures these limits
- provides communication mechanism so that services can talk among each other if required 

**2.Illusionist**
- gives the illusion of single infinite compute resource by abstracting away the hardware infrastructure
- provides the illusion that you need not care about underlying infrastructure (can run on a bare metal, in data centre, on the public cloud, or even hybrid cloud)
- gives the illusion that applications need not care about where they will be running

**3.Glue**
- provides common abstractions like Services, Ingress, auto scaling, rolling deployment , volume management
- comes with some security features: Namespaces, RBAC that applications can use transparently

**Why the need**
**1. Makes it easy to manage complex, evolving, and scalable architecture in an automated manner**

Once you start deploying multiple applications (e.g. Microservices) and need a consistent way for discovery, recovery, deployment, autoscaling, security, etc. for your applications — you need a container orchestration layer to manage them.
Kubernetes provides higher order constructs for building scalable applications:
- Mounting storage systems
**- Replicating application instances**
- Horizontal scalability
- Naming and discovery
**- Load balancing**

**2. Provides capabilities that you need for running production grade applications**

- Distributing secrets without environment variables or storing them in images
- Resource QoS for containers
- Liveness and readiness probes
- Termination and pre-termination messages
- Log access and inspection
- Support for introspection and debugging
**- Rolling updates**
- Identity and authorization

**3. Abstract away cloud providers so you can migrate relatively easily compared to if you are not using such abstraction**
- Runs anyware. Is a single solution for public, private, and hybrid cloud. It doesn't matter if deploymenttakes place over VMware, OpenStack, Azure Stack, AWS or Google Cloud. From the applications and developer’s perspective, it is completely transparent.
- Reduce risk of Infrastructure lock-in by providing abstractions that enable write once, run anywhere. 
- It is exactly the same service and the same containers across all.
- One tool to manage both linux and Windows environments.
  
**4. Supports wide variety of workloads like Batch, Stateless, Stateful, 12-factor, etc that are typically found in most software organisations. This gives reusable knowledge/skills that developers can use across different jobs.**

**5. Eases the life of operations team.**
- Helps ops team by automatically monitoring and rescheduling of the apps in the event of a hardware failure
- The focus of system administrator shifts from supervising individual apps to mostly supervising individual apps to mostly supervising Kubernetes and the rest of infrastructure, while Kubernetes itself take care of the apps
  
**6. K8S community is strong and growing.**
