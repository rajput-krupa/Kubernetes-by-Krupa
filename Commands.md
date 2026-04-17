# Commands For Cluster
### To create a cluster (kind):
kind create cluster [kind latest release paste here] --name=(clustername) --config= config.yml

### To get info about the cluster and context: 
kubectl cluster-info --context kind-(clustername)

### To see present nodes: 
kubectl get nodes

# Commands for .Yaml file
### To create/apply any file (.yaml):
kubectl create/apply -f filename.yml

# Commands for Pods
### To run a pod: just dry run (not actualy running, just to see output)
kubectl run nginx --image=nginx --dry-run=client

### To go inside the pod:
kubectl exec -it pod/podname --bash

## To describe the pod:
kubectl describe pod nginx-pod

## To see labels on pod: 
kubectl get pods nginx-pod --show-labels

## extended info about pod:
kubectl get pods -o wide

