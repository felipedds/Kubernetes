# Lesson 2 - Unraveling Kubernetes

# Start a cluster with 2 nodes in the driver
```
minikube start --nodes 2 -p felipe-multinode --kubernetes-version=v1.23.1
```

# Get the list of your nodes
```
kubectl get nodes
```

# Check the status of your nodes
```
minikube status -p felipe-multinode
```

# Look at our service, to know what URL to hit
```
minikube service list -p felipe-multinode
```

# Create other cluster with 2 nodes in the driver
```
minikube start --nodes 2 -p felipe2-multinode --kubernetes-version=v1.23.1
```

## List all resources in Kubernetes
```
kubectl api-resources
```

## Forward a local port to a port on the Pod
```
kubectl port-forward pod/pod1 8080:80
```

## Scale ReplicaSet
```
kubectl scale replicaset my-replicaset --replicas=10
```

## Change the image of container in Pod
```
kubectl set image deployment [NAME_DEPLOYMENT] [NAME_IMAGE]
```

# Execute a rollout in deployment
```
kubectl rollout history deployment [NAME_DEPLOYMENT]
```

# Execute a undo rollout in deployment
```
kubectl rollout undo deployment [NAME_DEPLOYMENT]
```