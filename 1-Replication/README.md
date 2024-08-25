## Replication:
Typically we want to replicate our containers i.e. our application for several reasons which include reliability, load balancing, and scaling. By having multiple versions of the application we prevent problems if one or more pods fail.

* https://www.geeksforgeeks.org/kuberneters-difference-between-replicaset-and-replication-controller/

### Create Replication Controller - rc-definition.yaml

- kubectl apply -f rc-definition.yml

### Create Replication Controller - replicaset-definition.yaml

- kubectl apply -f replicaset-definition.yml

#### Scale replicas

- kubectl replace -f replicaset-definition.yml
- kubectl scale --replicas=6 -f replicaset-definition.yml
- kubectl scale --replicas=6 replicaset my-nginx

#### Delete replicaset

- kubectl delete replicaset my-nginx


#### FAQ

* https://stackoverflow.com/questions/47369351/kubectl-apply-vs-kubectl-create