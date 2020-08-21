# argocd
This is test example with k8s

# Kubernetes
### Kubernetes strategy "Recreate" or "RollingUpdates" Deployment
```
# kubectl run nginx-deploy --image=nginx:1.16 replicas=1
# kubectl rolling-update nginx-deploy --image=nginx:1.17
# kubectl set image deployment nginx-deploy nginx-container=nginx:1.17
# kubectl rollout status deployment nginx-deploy
# kubectl rollout history deployment nginx-deploy
# kubectl rollout history deployment nginx-deploy --revision 1
# kubectl annotate deployment nginx-deploy kubernetes.io/change-cause="image updated to 1.17"
# kubectl rollout history deployment nginx-deploy
# kubectl set image deployment nginx-deploy nginx-container=nginx:1.17 --record
# kubectl describe deployment nginx-deploy |less
# kubectl rollout undo deployment nginx-deploy --to-revision=1
# kubectl set image deployment nginx-deploy nginx-container=nginx:latest
# kubectl rollout pause deployment nginx-deploy
# kubectl rollout resume deployment nginx-deploy
```
