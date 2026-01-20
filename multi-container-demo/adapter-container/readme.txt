kubectl cluster-info
kubectl apply -f adapter-demo.yaml
kubectl get pods
kubectl logs adapter-demo -c adapter
kubectl exec -it adapter-demo -c app -- cat /data/input.json
kubectl exec -it adapter-demo -c adapter -- cat /data/output.csv
kubectl delete pod adapter-demo