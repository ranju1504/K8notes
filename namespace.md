- default namespace 
- kube system namespace
- kube public namespace. 
- you can create your own namespace (like dev, prod)
- The resources in one namespace can refer to each other by their name 

`
    mysql.connect("db-service")
 `

 - To connect to an object in another namespace
 
`
    mysql.connect("db-service.dev.svc.cluster.local")
     
     cluster.local   - domain name 
     svc - sub domain
     dev - name space
     db-service - name of the service 
 `      
 
 
`
    kubectl create -f pod-definition.yml --namespace=dev
`

- To permanently change to another namespace as default:

`
    kubectl config set-contect $(kubectl config current-context) --namespace=dev   
`

 - Alternatively you can add the below in the yaml file

`
- metadata:
  - name: 
  - namespace: dev
   `
