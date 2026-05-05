# ConfigMap
- A Kubernetes API object used to store non-confidential data in key-value pairs.
- The main purpose of a ConfigMap is to decouple environment-specific configuration from container images. This allows you to build a single container image and run it in development, staging, or production just by swapping the ConfigMap.
- Can be done through **1.Imperative Way** and **2.Declarative Way**.

## Imperative Way:

<img width="489" height="54" alt="Screenshot 2026-05-05 at 3 42 02 PM" src="https://github.com/user-attachments/assets/2e3f0f6c-48e9-4ae4-8e14-4d5f4fa2d8aa" />
Now, need to parse it in the.yaml
inside the Container:
<img width="265" height="128" alt="Screenshot 2026-05-05 at 3 45 46 PM" src="https://github.com/user-attachments/assets/b563b483-980e-4021-bcff-f6e3772aaa9e" />

Usually a file is advisible as a configmap file. **configmap.yaml**
<img width="216" height="161" alt="Screenshot 2026-05-05 at 3 47 26 PM" src="https://github.com/user-attachments/assets/598078bc-d581-4ede-8957-034b10d74103" />

## Declarative Way:

