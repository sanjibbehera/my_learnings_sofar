## What is Kubernetes?
**Kubernetes** is an open-source container orchestration platform that automates the deployment, scaling, and management of containerized applications. It was originally developed by Google and is now maintained by the Cloud Native Computing Foundation (CNCF). Kubernetes provides a framework to run distributed systems resiliently, handling scaling and failover for applications, providing deployment patterns, and managing configurations.

## Key Features of Kubernetes
- Automated Rollouts and Rollbacks: Kubernetes can automatically roll out changes to your application or its configuration, monitoring application health to ensure all instances don’t fail simultaneously.
- Service Discovery and Load Balancing: Kubernetes can expose a container using the DNS name or its own IP address. If traffic to a container is high, Kubernetes can load balance and distribute the network traffic so that the deployment is stable.
- Storage Orchestration: Kubernetes allows you to automatically mount the storage system of your choice, such as local storage, public cloud providers, and more.
- Self-healing: Kubernetes restarts containers that fail, replaces containers, kills containers that don’t respond to your user-defined health check, and doesn’t advertise them to clients until they are ready to serve.
- Horizontal Scaling: Kubernetes can scale up or down the number of container instances based on CPU utilization or other application-provided metrics.
- Configuration Management: Kubernetes lets you manage configurations and secrets, helping you deploy and update secrets and application configuration without rebuilding your container images, and without exposing secrets in your stack configuration.

## What is EKS?
**Amazon Elastic Kubernetes Service** (Amazon EKS) is a managed service that eliminates the need to install, operate, and maintain your own Kubernetes control plane on Amazon Web Services (AWS). Kubernetes is an open-source system that automates the management, scaling, and deployment of containerized applications.

## Key Features of EKS
- Managed Kubernetes Control Plane: AWS manages the Kubernetes control plane, including the API servers and the etcd database. This means AWS handles the scalability, availability, and security of the control plane.
- Integration with AWS Services: EKS integrates with various AWS services to provide a seamless and powerful environment for your Kubernetes applications. For example, EKS integrates with Elastic Load Balancers (ELB) for load balancing, AWS Identity and Access Management (IAM) for access control, Amazon CloudWatch for logging and monitoring, and AWS CloudTrail for auditing.
- Networking: EKS supports Amazon VPC networking to provide isolation and control over Kubernetes networking.
- Security: EKS integrates with AWS IAM to provide fine-grained control over access to Kubernetes resources. EKS also supports AWS Key Management Service (KMS) for secrets management.
- Automatic Updates and Patching: AWS handles the updates and patching of the Kubernetes control plane.
- High Availability: EKS runs the Kubernetes control plane across multiple Availability Zones (AZs) to ensure high availability and fault tolerance.

## Whats in Control Plane?
The control plane manages the Kubernetes cluster. These components make global decisions about the cluster (for example, scheduling), as well as detecting and responding to cluster events.
- **ETCD**:
  - etcd is a consistent and highly-available key-value store used as Kubernetes’ backing store for all cluster data.
  - All cluster state and configuration data are stored in etcd, making it a critical component for cluster operation.
- **API Server**:
  - It exposes the Kubernetes API, which is used by all other components to communicate with the cluster.
  - It handles REST operations and provides the interface for the cluster management tools.
- **Controller Manager (kube-controller-manager)**
  - The controller manager runs controller processes that regulate the state of the cluster.
  - Examples of controllers include the ReplicaSet controller, which handles scaling of applications, and the node controller, which handles node lifecycle operations. The Deployment Controller will be managing Deployment objects and creating/modifying ReplicaSet objects. The Service Controller is responsible for configuring ClusterIP, NodePort, and LoadBalancer configuration based on Service objects. CronJob Controller(DaemonSet) is responsible for creating Job objects based on the Cron schedule defined in CronJob objects. StatefulSet Controller is responsible for creating Pods in a guaranteed order with a sticky identity.
- **Scheduler (kube-scheduler)**
  - The scheduler is responsible for placing pods on nodes.
  - It considers resource requirements, hardware constraints, affinity and anti-affinity specifications, data locality, inter-workload interference.
- 

## Whats in Data Plane?
Node components run on every node in the cluster and maintain the running pods and provide the Kubernetes runtime environment.
- **kubelet**
  - The kubelet is an agent that runs on each node in the cluster.
  - It ensures that containers are running in a pod by interacting with the container runtime.
  - The kubelet takes a set of PodSpecs and ensures that the described containers are running and healthy.
- **kube-proxy**
  - kube-proxy is a network proxy that runs on each node in the cluster.
  - It maintains network rules on nodes, which allow network communication to pods from inside or outside the cluster.
  - It uses Linux’s iptables or IPVS to manage IP routing and forwarding.
- **Container Runtime**
  - The container runtime is the software responsible for running containers.
  - Kubernetes supports several runtimes: Docker, containerd, CRI-O, etc.
  - The kubelet communicates with the container runtime to manage the lifecycle of containers.

## EKS Addons
- Amazon VPC CNI for Kubernetes
- CoreDNS: A flexible, extensible DNS server that can serve as the Kubernetes cluster DNS. The self-managed or managed type of this add-on was installed, by default, when you created your cluster. When you launch an Amazon EKS cluster with at least one node, two replicas of the CoreDNS image are deployed by default, regardless of the number of nodes deployed in your cluster. The CoreDNS Pods provide name resolution for all Pods in the cluster. You can deploy the CoreDNS Pods to Fargate nodes if your cluster includes an AWS Fargate profile with a namespace that matches the namespace for the CoreDNS deployment.
- kube-proxy: Maintains network rules on each Amazon EC2 node. It enables network communication to your Pods. The self-managed or managed type of this add-on is installed on each Amazon EC2 node in your cluster, by default.

## Access Management
- Grant access to Kubernetes APIs
  - IAM Role
  - IAM User
  - OpenID Connect (OIDC) provider
  - Kubernetes Service Accounts
  - EKS Pod Identities (Not for Fargate ATM): EKS Pod Identities provide the ability to manage credentials for your applications, similar to the way that Amazon EC2 instance profiles provide credentials to Amazon EC2 instances. Instead of creating and distributing your AWS credentials to the containers or using the Amazon EC2 instance's role, you associate an IAM role with a Kubernetes service account and configure your Pods to use the service account. Each EKS Pod Identity association maps a role to a service account in a namespace in the specified cluster. If you have the same application in multiple clusters, you can make identical associations in each cluster without modifying the trust policy of the role.

## Autoscaling
1. Karpenter
2. Cluster Autoscaler

## Cluster Management
1. Vertical Pod Aitoscaler
2. Horizontal Pod Autoscaler
3. Network Load Balancer
4. Aplication Load Balancer

## Deployment
1. Helm
2. ArgoCD
3. Kustomize

# Security
1. Certificate Signing
2. 

## Observability
1. Prometheus
2. CloudWatch
3. ADOT (AWS Distro for OpenTelemetry)
4. New Relic
5. Datadog

## Others
- Liveness Probe
- Readiness Probe
- Taints and Tolerations
- Node Selector and Node Affinity