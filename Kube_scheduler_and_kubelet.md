## Kube Scheduler 
  - Responsible for scheduling pods on nodes. 
  - Decides where to place the pods. 
  - Kubelet creates the pods 
  - The scheduler goes through 2 phases to identify the node for the pod.
  - First, it tries to filter the nodes that dont fit the profile of the pod(CPU and memory requested by pod)
  - Second, it uses a priority function to assign a score on scale 0 to 10. It calculates the amount of space on each node after placing the pod.
  - kubeadm installs scheduler as a pod on the kube system namespace. 
  
  ## Kubelet ( Captain on the ship)
  - Sole point of contact from the master.
  - It adds/removes containers based on instruction from the master
  - Kubelet requests the container runtime engine (docker) to load the image. 
  - kubelet monitors the pods and container and reports to the kube api server 
  - kubeadm doesnt install kubelet. 
  - Manually install the kubelet on the worker nodes. Download and run it a service. 
  
