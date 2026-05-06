## Access and Authorization
to see if any user had access: 
<img width="312" height="30" alt="Screenshot 2026-05-06 at 12 48 22 PM" src="https://github.com/user-attachments/assets/49bc30c7-0f48-4260-a4bb-91216b84c527" />
Now as this new user: adam, doesn't has any access to the pods, now to give him the access, we have to create the **Role** and **Role Binding**.

We will create a **Role** yaml. (instead of spec will create *rules*)
<img width="426" height="179" alt="Screenshot 2026-05-06 at 1 02 14 PM" src="https://github.com/user-attachments/assets/2073639c-7609-4ba6-93c4-7a1a3060ca22" />

Apply this role.yaml.
To see this role: ```kubectl get role```
To see in detail: ```kubectl describe role rolename```

**Now Role is created but not yet applied to which User**

For this, we have to create an another object, that is **RoleBinding**. For this we will create a another Yaml, *roleBinding.yaml*.

```
apiVersion: rbac.authorization.k8s.io/v1
# This role binding allows "jane" to read pods in the "default" namespace.
# You need to already have a Role named "pod-reader" in that namespace.
kind: RoleBinding
metadata:
  name: read-pods
  namespace: default
subjects:
# You can specify more than one "subject"
- kind: User
  name: adam # "name" is case sensitive
  apiGroup: rbac.authorization.k8s.io
roleRef:
  # "roleRef" specifies the binding to a Role / ClusterRole
  kind: Role #this must be Role or ClusterRole
  name: pod-reader # this must match the name of the Role or ClusterRole you wish to bind to
  apiGroup: rbac.authorization.k8s.io
```

Apply this binding.yaml

<img width="360" height="247" alt="Screenshot 2026-05-06 at 1 21 55 PM" src="https://github.com/user-attachments/assets/edd98ecd-36a8-4cfd-8ba3-385ab4ddf323" />

 This is binded and adam has got the access to this role.
 To see number of roles created.
 <img width="405" height="36" alt="Screenshot 2026-05-06 at 1 28 02 PM" src="https://github.com/user-attachments/assets/8776d527-0bfe-4a52-8365-b433d41e8ead" />

**How to get into any role and use as his credentials?**
<img width="446" height="69" alt="Screenshot 2026-05-06 at 1 30 16 PM" src="https://github.com/user-attachments/assets/54e43f98-90b3-47c4-a10f-fe9be8b70a3b" />
We have to make the cpntext now, 
<img width="513" height="52" alt="Screenshot 2026-05-06 at 1 38 56 PM" src="https://github.com/user-attachments/assets/92c77c47-f541-4458-a6cf-516480d3f906" />

when looking, Right now the context is different, we have to change it to adam.

<img width="557" height="291" alt="Screenshot 2026-05-06 at 1 37 11 PM" src="https://github.com/user-attachments/assets/2af0be38-daf9-40f6-a73c-11cae4b17d65" />

SO to change it,

<img width="557" height="161" alt="Screenshot 2026-05-06 at 1 38 33 PM" src="https://github.com/user-attachments/assets/66257c31-22be-4d40-9780-8f89026c4cfb" />


