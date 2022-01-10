## Kube Proxy 

- It is a process that runs on each node in the cluster
- Its job is to look out for new services. Every time a service is created, it creates rules for traffic to be forwarded to those services. 
- It uses IPTABLES rule.
- Can be installed in 2 ways. Download from kubernetes release page, extract and run. Or kubeadm installs it on the kube-system namespace. 
