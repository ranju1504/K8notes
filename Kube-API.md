## Kube API server

- Kube API server is the primary management component in K8
- kubectl utility reaches the kube API server. The server then authenticates the req and validates it. It then retrieves the data from the etcd cluster.
- For creating a pod object using POST command, the API server creates a pod-> updates the information in the etcd. updates the user that the pod is created. The scheduler monitors the api server. the scheduler identifies the right node to place the pod on and communicates this to the api server. 