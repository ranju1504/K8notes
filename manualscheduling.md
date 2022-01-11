## Manual scheduling 

- If there is no scheduler, the pod remains in pending state after it is created. 
- Without a scheduler, the easiest way to assign a node is by adding a nodeName field to the spec section of the definition file. 
- This can be done only at the creation time. 
- After a pod is created without a node assignment in the definition file, we have to create a binding object and send a POST request to the node's binding API. 

apiVersion:v1
kind: Binding 
metadata:
  name:nginx
target:
  apiVersion: v1
  kind: Node
  nodeName: node02
  
  
  curl  --header "Content-Type:application/json" --request POST --data '{"apiVersion":"v1", "kind":"Binding"...}http://$SERVER/api/v1/namespaces/default/pods/$PODNAME/binding/


-  
- 
