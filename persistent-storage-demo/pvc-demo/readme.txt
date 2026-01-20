kubectl cluster-info
kubectl apply -f pvc.yaml
kubectl apply -f deployment.yaml
kubectl get pods

# exec command in pod to save file data
# destroy pod and create new
# check data in volume

kubectl exec -it app-deployment-767ddb6bf4-7txm2 -- sh
echo "Hello persisted data" > /mnt/data/test.txt
cat /mnt/data/test.txt
exit

kubectl delete pod app-deployment-767ddb6bf4-7txm2
kubectl get pods
kubectl exec -it app-deployment-767ddb6bf4-rksk6 -- sh
cat /mnt/data/test.txt
exit

kubectl delete -f deployment.yaml
kubectl delete -f pvc.yaml 

