# homework3

# deployment codes
kubectl apply -f .\deployment_frontapp.yaml
kubectl apply -f .\deployment_backapp.yaml

# service codes
kubectl apply -f .\service_frontapp.yaml
kubectl apply -f .\service_backapp.yaml

# pod list
kubectl get pods

# describe
kubectl describe deployment backapp
kubectl describe deployment frontapp
kubectl describe svc backapp
kubectl describe svc frontapp