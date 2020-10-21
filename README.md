# kubernetes

## Kubernetes - Troubleshooting 

### Check accessibility:
```
curl http://web-service-ip:node-port
kubectl describe service web-service
```
### Check POD:
```
kubectl get pod
kubectl describe pod web
kubectl logs web
```
### Control Plane Failure:
```
kubectl get nodes
kubectl get pods
kubectl get pods -n kube-system
service kube-apiserver status
service kube-controller-manager status
service kube-scheduler status
service kubelet status
service kube-proxy status
kubectl logs kube-apiserver-master -n kube-system
```
### Work Node Failure:
```
kubectl get nodes
kubectl describe node workder-1
kubectl describe node workder-1
service kubelet status
sudo journalctl -u kubelet
openssl x509 -in /var/lib/kubelet/worker-1.crt -text
```
