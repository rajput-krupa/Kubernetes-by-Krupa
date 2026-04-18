# Service
To make the application available, services are used in Kubernetes.
So the app is accessible to the users and pods(frontend, backend, Databases) are able to communicate with each other.

So between the user and the pods, **Service** will act as a mediator. Makes sure that pods are listening to a certain ports. Loosely coupled.

<img width="462" height="245" alt="Screenshot 2026-04-18 at 1 23 34 PM" src="https://github.com/user-attachments/assets/c3f210eb-deae-48b1-a5ff-b3e4a07145ce" />


## Types of Services
- **ClusterIP**
- **NodePort**: - Service through which app would be exposed (externally) on particular port (*Nodeport*).
                <img width="450" height="251" alt="Screenshot 2026-04-18 at 1 43 18 PM" src="https://github.com/user-attachments/assets/9c58091b-baf1-4b28-a654-e0eb1e13241f" />
  - Application Exposed at: port: 300001 (*NodePort*-accessed by user).
  - Application listening internally at: port :80 (*TargetPort* - app listening to this internally) 
  - Application accessed by internal pods (frontend, backend, Dbase) and used by Service to communicate pods as mediator: port: 80 (*Port*)
  - Service load balances the traffic internally within port 80.
- **External names**
- **Load Balancer**
  
