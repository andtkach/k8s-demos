kubectl cluster-info
kubectl apply -f init-and-app-pod.yaml
kubectl get pods
kubectl logs init-app-demo -c init-container
kubectl logs init-app-demo
kubectl delete pod init-app-demo