**How the system kubernetes know that you are authorize or you have certain permission to access the Data??**

For this a yaml file is being created. 
kind: Config
In this yaml, First a **cluster** is mentioned, then the role **user** is mentioned and to connect both **context** is written. 
<img width="268" height="212" alt="Screenshot 2026-05-06 at 11 58 33 AM" src="https://github.com/user-attachments/assets/42036041-71ea-48e3-8988-6be9ecaf067f" />

<img width="524" height="245" alt="Screenshot 2026-05-06 at 11 59 33 AM" src="https://github.com/user-attachments/assets/9141b731-3037-4018-9900-ba4ede6385e4" />

1. ***ABAC***: (Attribute based Access control)---> Associate some set of permission to user,add that permissions to a policy file. Then add the file into API server config. As we have to start API server every time, we don't usually do this.
2. ***RBAC***: Here, we create a role, we assign certain permissions to that role, then we assign that role to a particular user, so every time we have change in the role, we just update the role. Users are not impacted.
3. ***Node***: Used by Nodes to interact with each other.
4. ***WebHook***: 3rd party system is used, which manages the permissions.
