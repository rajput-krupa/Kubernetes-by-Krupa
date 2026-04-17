# Commands For Kubernetes

## To create a cluster (kind):
kind create cluster [kind latest release paste here] --name=(clustername) --config= config.yml

## To get info about the cluster and context: 
kubectl cluster-info --context kind-(clustername)

## To see present nodes: 
kubectl get nodes

## To create/apply any file (.yaml):
kubectl create/apply -f filename.yml

## To run a pod: just dry run (not actualy running, just to see output)
kubectl run nginx --image=nginx --dry-run=client

## To go inside the pod:
kubectl exec -it pod/podname --bash

