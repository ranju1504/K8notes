## Kube API server

- Kube API server is the primary management component in K8
- kubectl utility reaches the kube API server. The server then authenticates the req and validates it. It then retrieves the data from the etcd cluster.
- For creating a pod object using POST command, the API server creates a pod-> updates the information in the etcd. updates the user that the pod is created. The scheduler monitors the api server. the scheduler identifies the right node to place the pod on and communicates this to the api server. The api server updates the etcd. The api server updates the kubelet. The kubelet creates the pod. The kubelet updates the api server. The api server then updates the etcd. 
- kubeadm installs the kube api server as a pod in the kube system namespace

## Kube Controller Manager 

- Kube controller is a process that continously monitors the state of the various components in the system and works towards bringing the system to the desired functioning state. 
- Watch status and remediate the situation
- Node controller checks the status of the nodes every 5 sec. It does that via kube api server. If it stops receiving heartbeat, then it marks the node as unreachable after waiting for 40 sec. 
- After marking it as unreachable, it waits for 5 min for it to come back up. If it doesnt come back up, it removes the pod from the node and provisions it on a healthy node. 
- Replication controller  ensures that a desired number of pods is available all the time.
- All the controllers are packaged as kube controller manager.
- kubeadm deploys the kube controller manager as a pod in the kube-system namespace. 
