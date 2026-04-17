# Replication Controller:
Docker container can not be ideally run standalone. Its a drawback of running Docker container.
As if application crashes at endpoint, its DONE!
So, an orchestration system is needed, to get a mechanism for autohealing the Application, or spin up new pod when it crashes. 

### Replication Controller
- Spins up a new pod (*identical pod*) when the pod crashes.
- Most of the time for high availability, even if the pod didn't crashes, it automatically spins up a new pod to scale the load.
- This is managed by *ReplicationController*  which make sure that the K8s resource is up and running all the time. Responsible for monitoring    resources.
  


