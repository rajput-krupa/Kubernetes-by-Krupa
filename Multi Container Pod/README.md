# Multi Container Pod:
Eg: We have an app running,(For i. Nginx)
So there are 2 pods (additional) which are running to support the Nginx-pod.
## 1. Init
- Runs before app container to do some initial tasks.
- Before the actual pod starts, **Init** container starts. Once it completes, app container starts.
- Shares resources of Pod.
## 2. Sidecar
- Always running with the app container as a support
- Provides certain input or provide output.
- Also referred as a "Helper Container".
  
      
