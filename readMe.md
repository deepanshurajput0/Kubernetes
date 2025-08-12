## Kubernetes Cluster

It is a group of machines working together to run containerized applications 

 ## Pods

1) - Pods are the smallest deployable units in Kubernetes.

2) -  Each pod typically contains one container (but can have more).

## Worker Nodes

Run your backend/frontend pods

## Master Node

Controls the cluster (scheduling, etc.)

Developer	Interacts with the master to deploy/manage apps

<img width="1687" height="788" alt="Screenshot 2025-08-08 005711" src="https://github.com/user-attachments/assets/127960c9-7049-4a0c-8ed4-477f684b0511" />

## Kubernetes Commands

- kind create cluster --name local
- kubectl get nodes
- kubectl get pods
- kubectl run nginx --image=nginx --port=80
- kubectl get pods
- kubectl logs nginx

## Deployment 

In kubernetes deployment is the resource object which manages the lifecycle of your application pods ensure they are always running in desired state 
Declarative - you can run 3 replicas of a specific image 
Self healing - If any pod goes down or crashes then it automatically spin up new pod and replcae it with old one
rolling updates - it can update your old pods with new pods without having any downtime 
rollback - if something happen wrong with new inmage then it will be revert back to previous image


