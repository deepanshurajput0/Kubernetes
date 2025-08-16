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

- Declarative - you can run 3 replicas of a specific image 
- Self healing - If any pod goes down or crashes then it automatically spin up new pod and replcae it with old one
- rolling updates - it can update your old pods with new pods without having any downtime 
- rollback - if something happen wrong with new inmage then it will be revert back to previous image

## Replicas 

replicas simply a number of copies of pods you want to running at same time 

## Why we use Replicas 

- High availablity - if any pod got crashed then we have other pods which are running continuosly and it avoids downtime
- Load distribution → Multiple replicas allow incoming requests to be spread across pods (using a Service), improving performance and avoiding overload on a single pod.

## Service 

In Kubernetes, a Service is an abstraction that defines a logical set of Pods and a policy by which to access them. Pods are ephemeral (they can die and be replaced), so Services provide a stable way to reach these dynamic Pods. Essentially, a Service acts as a network endpoint that stays constant even when the underlying Pods change.


<img width="1920" height="1080" alt="Screenshot (308)" src="https://github.com/user-attachments/assets/67681181-0113-4655-8fbb-2a86fd82e12f" />

<img width="1920" height="1080" alt="Screenshot (307)" src="https://github.com/user-attachments/assets/b4310d11-8168-40dd-85be-d41b493d9074" />


## Types of Services

    ClusterIP (default)

        Exposes the service internally inside the cluster.

        Other Pods in the cluster can access it via the service name.

        Example: Internal APIs.

    NodePort

        Exposes the service on a static port on each Node.

        Can be accessed externally via NodeIP:NodePort.

    LoadBalancer

        Works with cloud providers to provide an external load balancer.

        Exposes the service to the internet.

        Useful for production apps.

    ExternalName

        Maps a service to an external DNS name.

        No proxying; just DNS resolution.


# Nginx 

## Forward Proxy 

<img width="1185" height="711" alt="Screenshot 2025-08-14 130246" src="https://github.com/user-attachments/assets/a880fc40-2e69-424b-8867-31a2f9a18330" />

## Reverse Proxy

<img width="1331" height="753" alt="Screenshot 2025-08-14 130922" src="https://github.com/user-attachments/assets/c5aad137-17d4-4237-8132-3a653d22a282" />



Web server mode: Nginx mainly serves static files, caches content, and proxies requests to backend servers.

Load balancer mode: Nginx distributes traffic across multiple backend servers. Big companies often combine Nginx with dedicated load balancers for advanced traffic handling.




