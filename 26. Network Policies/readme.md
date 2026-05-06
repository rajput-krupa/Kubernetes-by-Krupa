# Network Policies:

For eg: For a 3 tier app. User access front end , frontend contacts Backend and backend too Dbase. 
For all incoming requests its called the "***Ingress***"

<img width="695" height="278" alt="Screenshot 2026-05-06 at 6 23 05 PM" src="https://github.com/user-attachments/assets/e994f653-ec63-4ac4-bf99-e3e9c7c2876c" />

- Incoming request: ***Ingress***
- Outgoing Request: ***Egress***
- They all are communicating with each other with the **Container Network Interface**. Creates a pod of CNI in each pods, so they can communicate.
- But here if we don't want the frontend pod to contact directly the database, and have policies in between, we will need ***Network Policies***.
- Network policies impliment certain rules, restrictions to the pod networking so that not everything is connected to each other by default.
- But here, not every CNI supports Network Policies

*So to implement any cluster related issue in the or permission restric we have to implement the cluster-worker Yaml.

- <img width="557" height="69" alt="Screenshot 2026-05-06 at 6 34 54 PM" src="https://github.com/user-attachments/assets/dcff8c30-2fa6-4163-a56f-dabb7cc9a532" />

Now this yaml is created for any matching labels and whom they can interac with each other for eg, here they can interac if the pod = nginx , label = nginx
<img width="248" height="207" alt="Screenshot 2026-05-06 at 7 10 39 PM" src="https://github.com/user-attachments/assets/e5d9c5bb-1b6d-457e-9015-a44a45cde683" />

