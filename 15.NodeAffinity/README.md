   # Node Affinity
    - Taints and tollerations has some limitations on adding multiple conditions on the pods. So NodeAffinity comes into the picture.
    - Can add multiple conditions through NodeAffinity.
    - How It Works???? ---> Nodes has labels (with Operators), it tries to match with the affinity set on pods.
    - WHat if the labels are changed?? --->
    
<img width="660" height="162" alt="Screenshot 2026-04-30 at 7 56 02 AM" src="https://github.com/user-attachments/assets/c54ad80e-70a9-42b5-878b-fab9de87720e" />

**requiredDuringSchedulingIgnoredDuringExecution** - Make sure to schedule the pod on matching label, ignore during the execution.
**preferredDuringSchedulingIgnoredDuringExecution** - Prefers its matching the label. Even if not matching, it will scheduling ignore during the execution
