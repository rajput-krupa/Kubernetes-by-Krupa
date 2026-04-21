# Namespaces:
Level of isolation within cluster, for seperation of objects and resources. 
When namespace is not specified in a resource while creation, by default goes to **Default** Namespace.
Can assign different RBACs. Security. Isolation
Resources Can access each other in Namespace through Hostname.
Within different Namespace, they communicate with "FQDN- Fully Qualified Domain Name "



# Commands:
To create:
1. Imperative way: ```kubectl create deploy nginx-demo --image=nginx -namespace demo ```
2. Declarative Way: nginx-demo.yaml
