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

# ingress
kubectl apply -f .\ingress.yaml

# delete all resorse (svc/pod)
kubectl delete all -l training=block3

# logs
kubectl logs -l app=frontapp --all-containers=true   -> for frontapp
kubectl logs -l app=backapp --all-containers=true   -> for backapp

# Command(s) for checking the logs of the backapp application
kubectl logs -l app=backapp --all-containers=true

# ONE kubectl command which lists all resources related to the frontapp
kubectl get all -l homework=frontapp

# ONE kubectl command which can delete all resources for both applications


