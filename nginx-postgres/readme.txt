kubectl create configmap web-content --from-file=html --dry-run=client -o yaml > k8s-manifests/web-content-configmap.yaml

kubectl apply -f k8s-manifests

kubectl get deploy,svc,pvc

open web: http://localhost:30081
