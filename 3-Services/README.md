## Kubernetes Services

- Kubernetes Services are an essential component in Kubernetes that facilitate communication between different parts of an application and between applications and external users. They act as an abstraction layer that connects a group of pods to each other or to the outside world, ensuring seamless interaction within a Kubernetes cluster.

## Key Features of Kubernetes Services:
Internal and External Communication: Services enable different groups of pods, such as frontend and backend pods, to communicate with each other. They also allow external users to access applications running inside the cluster.

### Types of Services:

NodePort: Exposes a service on a specific port on each node in the cluster, allowing external access to the application.

ClusterIP: Creates a virtual IP within the cluster, facilitating communication between different services internally.

LoadBalancer: Automatically provisions a load balancer to distribute traffic across multiple pods, typically used in cloud environments.

### Load Balancing: 
Services automatically distribute incoming traffic across multiple pod instances, providing built-in load balancing without requiring additional configuration.

### Automatic Updates: 
When pods are added or removed, the service is automatically updated to include or exclude the relevant pods, making it highly adaptive and reducing the need for manual intervention.

- In summary, Kubernetes Services are a critical tool for managing the flow of traffic between different components in a Kubernetes environment, ensuring that applications are accessible, scalable, and resilient.


#### Get all the service from all the namespaces 
- kubectl get services --all-namespaces

#### Get external URL for the service to connect
- minikube service my-nginx --url

### EXTERNAL-IP is always none and unable to reach to Service from Host machine
* https://github.com/kubernetes/minikube/issues/3966