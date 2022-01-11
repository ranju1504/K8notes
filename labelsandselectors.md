##Labels and Selectors

```sh
  kubectl get pods --selector app=App1 
```


## Taint and Toleration:

- Those nodes that are tolerant to the taint on the node will be placed on the node. 
- Taint on nodes and toleration on pods 

```sh
  kubectl taint nodes node-name key:value:taint-effect
  kubectl taint nodes node01 app:blue:NoSchedule 
``` 

Effects can be Noschedule, PreferNoSchedule or NoExecute 

- Add tolerations to the pod

```
  tolerations:
   - key: "app"
     operator: "Equal"
     value: "blue"
     effect: "NoSchedule"
 ```

