## Pods

- Containers are encapsualted in a kubernetes object called pods. 
- A pod is a single instance of the appln. It is the smallest object in the kubernetes. 
- Pods usually have 1:1 relationship with the containers. 
- Single pod can have multiple pods(usually not of same kind). Sometimes helper containers live along side the appln in another container in the same pod.
- Scaling up = additional pods. 

```sh
   kubectl run nginx --image nginx
   kubectl get pods 
 ```  
