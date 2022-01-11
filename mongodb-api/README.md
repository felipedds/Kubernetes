# API with MongoDB

## Create Namespace (Prod, Hom, Dev)
```
kubectl create namespace prod-api-produto
kubectl create namespace hom-api-produto
kubectl create namespace dev-api-produto
```

## Create Deployment(deployment.yml) and Service(service.yml)
```
kubectl apply -f ./api/ -f ./mongodb/ --namespace prod-api-produto
kubectl apply -f ./api/ -f ./mongodb/ --namespace hom-api-produto
kubectl apply -f ./api/ -f ./mongodb/ --namespace dev-api-produto
```

## Create Secret (Prod, Hom, Dev)
```
kubectl apply -f ./prod-secret/ --namespace prod-api-produto
kubectl apply -f ./hom-secret/ --namespace hom-api-produto
kubectl apply -f ./dev-secret/ --namespace dev-api-produto
```

## Verify Namespace created 
```
kubectl get namespace
```

## Verify Services created (Prod, Hom, Dev)
```
kubectl get service --namespace prod-api-produto
kubectl get service --namespace hom-api-produto
kubectl get service --namespace dev-api-produto
```

## Verify Pods created (Prod, Hom, Dev)
```
kubectl get pods --namespace prod-api-produto
kubectl get pods --namespace hom-api-produto
kubectl get pods --namespace dev-api-produto
```

## Delete Namespace created (Prod, Hom, Dev)
```
kubectl delete namespace prod-api-produto
kubectl delete namespace hom-api-produto
kubectl delete namespace dev-api-produto