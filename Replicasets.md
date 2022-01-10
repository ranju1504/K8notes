## Replica sets

- Helps with high availability. 
- Makes sure specific number of pods is running all the time.
- It spans across multiple nodes. 
- It can manage pods that were not created as part of the replica set as long as it matches the label name. 

```sh
  apiVersion: apps/v1
  kind: ReplicaSet
  metadata:
    name: myapp-replicaset
    labels:
      app: myapp
      type: front-end
  spec:
    template:
      metadata:
         name: myapp-pod
         labels:
            app: myapp
            type: front-end 
         containers:
            - name: nginx-container
              image: nginx
    replicas: 3
    selector:
      matchLabels:
        type: front-end 
 
```


```sh
  kubectl create -f replicaset-definition.yaml 
 
```
