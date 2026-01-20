
kubectl apply -f storage-class.yaml
kubectl apply -f pv.yaml
kubectl apply -f pvc.yaml
kubectl apply -f deployment.yaml
kubectl get pods

kubectl exec -it local-storage-demo-5c655b8dfd-vn8lw -- ls /mnt/data
kubectl exec -it local-storage-demo-5c655b8dfd-vn8lw -- sh
cat /mnt/data/message.txt
exit

kubectl delete pod local-storage-demo-5c655b8dfd-vn8lw

kubectl get pods
kubectl exec -it local-storage-demo-5c655b8dfd-nvbjx -- sh
cat /mnt/data/message.txt
exit
