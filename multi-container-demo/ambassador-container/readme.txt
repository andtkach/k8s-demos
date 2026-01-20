kubectl cluster-info
kubectl apply -f ambassador-demo.yaml
kubectl get pods
kubectl logs ambassador-demo -c app
kubectl delete pod ambassador-demo