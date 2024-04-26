# DEPLOYING APPLICATION INTO KUBERNETES CLUSTER
In this project, I will initiate the deployment of applications within a Kubernetes (K8s) cluster. Kubernetes is a complex system with numerous components, working with multiple layers of abstraction that separate your application from the underlying host machines where it is executed.

we will explore and witness the following aspects in action:

Implementing the deployment of software applications using YAML manifest files, featuring various Kubernetes objects, including:

    - Pods
    - ReplicaSets
    - Deployments
    - StatefulSets
    - Services (ClusterIP, NodeIP, Loadbalancer)
    - Configmaps
    - Volumes
    - PersistentVolumes
    - PersistentVolumeClaims
    And more.

- Understanding the distinctions between stateful and stateless applications.

- Demonstrating the deployment of MySQL as a StatefulSet and providing a rationale for this choice.

- Identifying the limitations associated with deploying applications directly using YAML manifests in Kubernetes.

- Introducing Helm templates, exploring their components, and highlighting the significance of semantic versioning.

- Converting all the existing .yaml templates into a Helm chart for more streamlined management.

- Deploying additional tools on AWS Elastic Kubernetes Service (EKS) using Helm charts, which include:

    - Jenkins
    - MySQL
    - Ingress Controllers (Nginx)
    - Cert-Manager
    - Ingress configurations for Jenkins and the primary application
    - Deploying Monitoring Tools, such as Prometheus and Grafana.

 Exploring the concept of Hybrid CI/CD by integrating various tools like Gitlab CI/- CD and Jenkins. Additionally, we'll delve into GitOps principles using Weaveworks Flux.

When utilizing a Kubernetes cluster, the available options vary depending on its intended purpose.

Numerous organizations choose Managed Service solutions for various compelling reasons, such as:

    - Less administrative overheads
    - Reduced cost of ownership
    - Improved Security
    - Seamless support
    - Periodical updates to a stable and well-tested version
    - Faster cluster spin up

However, there is usually strong reasons why organisations with very strict compliance and security concerns choose to build their own Kubernetes clusters. Most of the companies that go this route will mostly use on-premises data centres. When there is need to store data privately due to its sensitive nature, companies will rather not use a public cloud provider. Because, if they do, they have no idea of the physical location of the data centre in which their data is being persisted. Banks and Governments are typical examples of this.

Some setup options can combine both public and private cloud together. For example, the master nodes, etcd clusters, and some worker nodes that run stateful applications can be configured in private datacentres, while worker nodes that require heavy computations and stateless applications can run in public clouds. This kind of hybrid architecture is ideal to satisfy compliance, while also benefiting from other public cloud capabilities.

![alt text](images/22.1.png)
