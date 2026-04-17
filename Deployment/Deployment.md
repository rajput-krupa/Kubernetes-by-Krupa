# Deployment
As a user Deployment is created, and then under deployment ReplicaSets are created.
<img width="536" height="424" alt="ChatGPT Image Apr 17, 2026, 04_25_12 PM" src="https://github.com/user-attachments/assets/40138766-398e-4878-8a8b-7921526bae22" />

*For Instance*
If a change : Version , has to be done. If Done on Replicaset, it will apply the change and recreate the pods all at once. 
(cx will face a huge downtime.)

So, even though will rolling out the changes to live environment; Users should not be impacted.

- Deployment will make the changes in a rolling update pattern.
- Updates pod, while the update is up, traffic is redirected to another available/active pods. vice Versa
- Can also spin a new pod if needed.
