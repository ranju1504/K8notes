## ETCD

  - Distributed reliable key value store 
  - Stores information about the cluster - nodes,pods, configs, secrets, accounts, roles, bindings and others. 
  - Any change made to the cluster (like adding nodes, deploying pods) are added to the etcd. 
  - In a manual setup, download and install etcd on the master node 
  - etcd listens on advertise-client-urls, default port 2379
  - If you use kubeadm to set up cluster , kudeadm installs etcd server as a pod in the kube-system namespace. 
  
      ` kubectl get pods -n kube-system `
     --> you will see etcd-master listed. 
  - To list all keys stored by Kubernetes, 
  - 
      ` kubectl exec etcd-master -n kube-sytem etcdctl get / --prefix -keys -only `
