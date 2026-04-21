# Daemonset
- Unlike replica (That are created on each nodes)
- A ReplicaSet maintains a specific number of pod replicas, often spread across nodes, to ensure high availability.
- A DaemonSet ensures one copy of a pod runs on every (or selected) worker node in the cluster.
- An RS may place multiple replicas on one node, while a DS ensures exactly one pod per node.
  
- <img width="776" height="439" alt="Screenshot 2026-04-21 at 10 17 51 AM" src="https://github.com/user-attachments/assets/b697f81f-eeba-48e8-ab80-bdb8c3925c10" />

- Automatically when a new node is added, it adds a pod copy fot that node. And id deleted the node, replica is also deleted.
  
