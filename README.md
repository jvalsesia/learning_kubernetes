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

## Check the healt of a pod by looking at the event logs
```sh
kubectl describe pod pod-info-deployment-757cb75bbb-jnmgx
```
