kubectl cluster-info
kubectl apply -f app-with-logger.yaml
kubectl get pods
kubectl logs app-with-logger -c logger
kubectl delete pod app-with-logger 