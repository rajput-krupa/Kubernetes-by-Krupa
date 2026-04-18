
# Service
To make the application available, services are used in Kubernetes.
So the app is accessible to the users and pods(frontend, backend, Databases) are able to communicate with each other.

So between the user and the pods, **Service** will act as a mediator. Makes sure that pods are listening to a certain ports. Loosely coupled.

<img width="462" height="245" alt="Screenshot 2026-04-18 at 1 23 34 PM" src="https://github.com/user-attachments/assets/c3f210eb-deae-48b1-a5ff-b3e4a07145ce" />


## Types of Services
- **ClusterIP**: - In order to communicate with for eg; Backend pod to frontend pod. It will go through a cluster IP.

  - <img width="478" height="209" alt="Screenshot 2026-04-18 at 5 37 57 PM" src="https://github.com/user-attachments/assets/2c0f05b9-cbe8-4189-8f14-ee7e3c594fb3" />

  - Can access the services or pods using clusterIP name or IP of cluster IP.
  - Cluster IP can be accessed by : *kubectl get svc*
  - If need to create a one more ClusterIP: ***can be done similar like nodePort.yaml***, remove type: nodePort.
  - 

<img width="675" height="76" alt="Screenshot 2026-04-18 at 5 36 36 PM" src="https://github.com/user-attachments/assets/6649666c-52f8-442e-9d4b-4d9bbd04d862" />




- **NodePort**: - Service through which app would be exposed (externally) on particular port (*Nodeport*).
                <img width="450" height="251" alt="Screenshot 2026-04-18 at 1 43 18 PM" src="https://github.com/user-attachments/assets/9c58091b-baf1-4b28-a654-e0eb1e13241f" />
  - Application Exposed at: port: 300001 (*NodePort*-accessed by user).
  - Application listening internally at: port :80 (*TargetPort* - app listening to this internally) 
  - Application accessed by internal pods (frontend, backend, Dbase) and used by Service to communicate pods as mediator: port: 80 (*Port*)
  - Service load balances the traffic internally within port 80.
  - Next step, get node id: In this case: **172.19.0.9**
  - Run command: curl 172.19.0.9:30001 (On web: localhost://30001)
 
    
- **External names**: For internal apps to refer to the DNS of application, *External Names* are used
  
- **Load Balancer**: Every pod has an IP assigned, when pod restarts, Ip changes (pod IP is not static). So, can't access the pod from IP address. Not even internally.
  - So **LoadBalancer** is used, it will place all pods in backend of the load balancer.
  - Now, whenever user access the app, they don't have to access seperate ip of pods, just hit the load balancer and it will distribute traffic accross different pods. App spins up!!
  - We provision external Load balancer, then can use service type as "*Loadbalancer*" inside k8s and refer it.
    <img width="488" height="183" alt="Screenshot 2026-04-18 at 6 28 58 PM" src="https://github.com/user-attachments/assets/b2265b57-692c-4ca8-9e6d-ae89a1460b26" />
  
