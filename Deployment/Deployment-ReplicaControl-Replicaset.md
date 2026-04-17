# Replication Controller:
Docker container can not be ideally run standalone. Its a drawback of running Docker container.
As if application crashes at endpoint, its DONE!
So, an orchestration system is needed, to get a mechanism for autohealing the Application, or spin up new pod when it crashes. 

### Replication Controller
- Spins up a new pod (**identical pod**) when the pod crashes.
- Most of the time for high availability, even if the pod didn't crashes, it automatically spins up a new pod to scale the load. **Highly Scalable**
- This is managed by **ReplicationController**  which make sure that the K8s resource is up and running all the time. Responsible for monitoring    resources.
- Replication controller is responsible for redirecting the traffic to active pods. *(It has a logic algorithm)*
- If the number is mentioned it always make sure, that atleast that no of replicas are always up and running. **Highly Available**
  <img width="631" height="331" alt="Screenshot 2026-04-17 at 2 45 04 PM" src="https://github.com/user-attachments/assets/d18e693e-c156-4063-9321-9b5ba0d6660e" />


## If (Worker) Node is Out of Capacity of Pods.
- Then it spins up a new node and provision pod in the new node.
- Replication controller can spin up multiple nodes. (manual for now) can be done by automatically.


  


