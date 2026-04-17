# Pods
The App container is inside the POD. POD is the smallest unit of Kubernetes architecture. Resides in Worker Node.

## How to flow works? 
User interacts with the API Server which is in control plane node. With help of client utility (In Kind - Kubectl)to provision, update or get details from cluster.

## 2 Ways of creating POD. (Imperative & Declarative)
- Imperative
  Simply instructing API Server or Kubectl utility to run or do specific thing. (running simply command)
- Declartive
  Creating a configuration file (JSON / YAML).
  Set desired state of object. (with specific details)
  Then run Kubectl apply/run command.    
  
