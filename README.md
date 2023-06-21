# learning_kubernetes
Learning Kubernetes

## Create a namespace
```sh
kubectl apply -f namespace.yaml
```

## Deploy an application
```sh
kubectl apply -f deployment.yaml
kubectl get pods -n dev-namespace
```
