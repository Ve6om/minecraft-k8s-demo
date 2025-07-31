# Minecraft Kubernetes Server
###  Kubernetes manifests to deploy a Paper Minecraft server on a k3s cluster. Uses persistent storage on the host.

## Setup
1. Create directory `/home/kubeuser/mc-server-data/server1` on the node and chown permissions.
2. Apply the manifests in order:
```bash
kubectl apply -f mc-pv.yaml
kubectl apply -f mc-pvc.yaml
kubectl apply -f mc-deployment.yaml
kubectl apply -f mc-service.yaml
```
3. Check pod status and logs to verify the server is running.

## Connect
Use your node’s IP and the exposed port (default 25565).