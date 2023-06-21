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

## Check the health of a pod by looking at the event logs
```sh
kubectl get pods -n dev-namespace
kubectl describe pod pod-info-deployment-757cb75bbb-jnmgx
```

## Check that your application is working with BusyBox
```sh
kubectl config set-context --current --namespace=default
kubectl apply -f busybox.yaml
kubectl get pods -n default -o wide
kubectl exec -it busybox-6b95744666-m7j8q -- /bin/sh
kubectl get pods -n dev-namespace -o wide
```
Inside BusyBox runing in default namespace you can run wget using any dev-namespace Pod IPs, for example:
```sh
wget 10.244.2.3:3000
cat index.html
exit
```
Where, 3000 is the Pods port.



