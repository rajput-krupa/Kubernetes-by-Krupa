# Requests and Limits
Every node has certain limits to accomodate the pods 
For eg: 
<img width="530" height="341" alt="Screenshot 2026-04-30 at 8 41 15 AM" src="https://github.com/user-attachments/assets/f772c00e-46c8-4fb2-9a1b-2d0c9ed17f64" />

After this is full, if any pods comes up, it will say ERROR "**Insufficient Resources**".

AFter this if one pod is taking the whole memory and resources it will say ERROR "**Out Of Resources**".
If more, node crashes and throws : "**OOM**"

So, just this scenerio doesn't comes up, to avoid we specify **Requests and Limits** in the pod, so now whenever the pod is taking more memory, the POD crashes, not the node.
<img width="290" height="95" alt="Screenshot 2026-04-30 at 8 49 11 AM" src="https://github.com/user-attachments/assets/3149260e-6161-41fa-bced-c754bd2154d5" />

