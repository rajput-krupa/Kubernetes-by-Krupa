   # Node Affinity
    - Taints and tollerations has some limitations on adding multiple conditions on the pods. So NodeAffinity comes into the picture.
    - Can add multiple conditions through NodeAffinity.
    - How It Works???? ---> Nodes has labels (with Operators), it tries to match with the affinity set on pods.
    How to set a label to node : 
   <img width="479" height="75" alt="Screenshot 2026-04-30 at 8 12 19 AM" src="https://github.com/user-attachments/assets/77c99488-d87b-43a1-a496-653c4503f44b" />

    - WHat if the labels are changed?? --->
    
<img width="660" height="162" alt="Screenshot 2026-04-30 at 7 56 02 AM" src="https://github.com/user-attachments/assets/c54ad80e-70a9-42b5-878b-fab9de87720e" />

**requiredDuringSchedulingIgnoredDuringExecution** - Make sure to schedule the pod on matching label, ignore during the execution.

<img width="461" height="167" alt="Screenshot 2026-04-30 at 8 04 44 AM" src="https://github.com/user-attachments/assets/50571b86-2868-4643-88d7-9f48a1d134f9" />

**preferredDuringSchedulingIgnoredDuringExecution** - Prefers its matching the label. Even if not matching, it will scheduling ignore during the execution
<img width="240" height="85" alt="Screenshot 2026-04-30 at 8 16 23 AM" src="https://github.com/user-attachments/assets/42eef1dc-139b-49ce-b89f-12476fe5d4c6" />

Node Affinity and Taints and Tollerations Both are used to make sure our pods are scheduled to correct Nodes.
