# Static pods:
- Control plane components that are not managed by **Scheduler**.
- On Cloud platforms, Control Plane is a virtual machine.
- All the control plane components are pods, but ****static pods****

<img width="432" height="304" alt="Screenshot 2026-04-21 at 1 48 11 PM" src="https://github.com/user-attachments/assets/773d5c2b-04b7-4f3f-8ce2-6541e3a23db3" />



# Manual Scheduling:
- Apart from the control plane schedular, there is a manual way to schedule pods, that's "**Manual Scheduling**"

## How manual Scheduling works??
- Schedular goes to the pods which are in pending state.
- Scans the pending pods. Looks for a pod that doesnot have a **Selector field** which doesn't have a **NodeName** specified.
- Because the one which has the node name specified knows what to do and it already has task allocated.
- It will catch a pod that doesn't have anything specified.
- ### How to particularly schedule a pod specific.
- While creating the resource, under spec > Containers > add field "nodeName" and mention name of the pod. so scheduled on same pod.

  <img width="467" height="111" alt="Screenshot 2026-04-21 at 2 14 57 PM" src="https://github.com/user-attachments/assets/5fc174de-9d05-41d8-bd2e-1ecbf87e7126" />




  # Labels:
  - Part of **metadata**. Helps in filtering the particular resource. Specifically part of **resource**.
  - Inside the **spec**. Its pod specific.
  - In **Selector**. Matches the label from pod to Deployment.


  # Namespace :
  Logical seperation of resources.
  
  
