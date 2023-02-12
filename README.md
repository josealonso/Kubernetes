### Kubernetes

It is the most popular containers orchestration tool.

Features:

- High Availability or no downtime
- Scalability or high performance
- Disaster recovery - backup and restore

### Architecture

A cluster consists of:

a master node and a number of worker nodes

#### Master node

Runs different processes:

- API Server: it is the entrypoint to the cluster.
- Controller manager: keeps track of whats happening in the cluster
- Scheduler
- etcd key-value storage: 

#### Virtual Network

It creates one unified machine for all the nodes in the cluster.

