- default namespace 
- kube system namespace
- kube public namespace. 
- you can create your own namespace (like dev, prod)
- The resources in one namespace can refer to each other by their name 

 '''
 mysql.connect("db-service")
 '''

 - To connect to an object in another namespace

 mysql.connect("db-service.dev.svc.cluster.local")


