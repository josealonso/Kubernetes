### Kubernetes

It is the most popular containers orchestration tool.

Features:

- High Availability or no downtime
- Scalability or high performance
- Disaster recovery - backup and restore

### Architecture

A cluster consists of:

a master node and a number of worker nodes

### Master node

Runs different processes:

- API Server: it is the entrypoint to the Kubernetes cluster.
- Controller manager: keeps track of whats happening in the cluster
- Scheduler: it ensures Pods placement.
- etcd key-value storage: it holds the state of the Kubernetes cluster.

### Virtual Network

It creates one unified machine for all the nodes in the cluster.

### Worker nodes

These nodes are much bigger and have more resources than the master node, 
because they are running the applications inside of them.

**POD**

Smallest unit of Kubernetes
Abstraction over container.
Usually one app per Pod.
Each Pod gets its own IP address. 
They are ephimeral.

**SERVICE**

Permanent IP address and load balancer.
Its lifecycle is not connected to that of Pod.

**INGRESS**

Used to route traffic into the cluster.

**CONFIGMAP**

External configuration of your application.

**SECRET**

Used to store secret data.
Base64 encoded.

**VOLUMES**

Kubernetes does not manage any data persistance.

**DEPLOYMENTS**

Abstraction of Pods.

**STATEFUL SET**

It makes sure there are no databases inconsistencies. 
However, databases are often hosted outside of the Kubernetes cluster.

### Minikube

It is one-node Kubernetes cluster, open source, with Docker pre-installed. 
It runs on a Virtual Box or some other hypervisor.

### kubectl

It is a command line tool for **any** Kubernetes cluster.

Common commands:

`kubectl create deployment`

`kubectl get nodes | pod | services | replicaset | deployment`

`kubectl logs [pod name]`
`kubectl exec -it [pod name] --bin/bash`
`kubectl describe pod [pod name]`

`kubectl apply -f [file name]`
`kubectl delete -f [file name]`

### Example with minikube and kubectl

`minikube start`

`kubectl apply -f mongo-secret.yaml`
`kubectl get secret`

Reference the secret values in the deployment file

`kubectl  apply -f mongodb-deployment.yaml`
