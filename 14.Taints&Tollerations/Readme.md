# Taints and Tolerations: *key value pair*
- If taint is set into some nodee for eg: (gpu=true), so we can't schedule any pod on that particular node.
- Even if it is tainted and we need to schedule on the same node, matching **Toleration** should be set on the *pod*.
- Toleration has **Effect** - Scheduling type. Can be either: NoSchedule (only new pods), NoExecute (existing/newer pods), preferNoSchedule (No guarantee).
- Even if a particular node has a tolleration, it doesn't prevents it to be scheduled on other nodes.
