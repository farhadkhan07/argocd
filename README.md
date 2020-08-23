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

### Persistent Volumes and Claims in Kubernetes
```
1. Create a PV
2. Create a PVC
3. POD thatr use PVC -- > PV
4. Dynamic Provision Storage Class

ReclaimPolicy
1. Retain
2. Recycle
3. Delete

Access Mode:
1. RWO 
2. RWM
3. RO

kubectl get pv,pvc,pod
kubectl describe pv pv-volume
kubectl describe pvc pvc-claim
kubectl exec pod-busybox-pvc ls
kubectl exec pod-busybox-pvc ls mydata
kubectl exec pod-busybox-pvc touch /mydata/hello
kubectl exec pod-busybox-pvc touch /mydata/hello2
kubectl exec pod-busybox-pvc ls /mydata
```
