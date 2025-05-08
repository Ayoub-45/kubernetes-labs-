# Kubernetes Deployment with Rolling Updates - NGINX

This project demonstrates how to deploy an NGINX container to a Kubernetes cluster using a Deployment and perform rolling updates across different image versions.

---

## 🧱 Initial Setup

We begin with deploying `nginx:1.22.1` using a Kubernetes Deployment manifest.

### nginx-deployment.yaml

```yaml
apiVersion: apps/v1
kind: Deployment
metadata:
  name: nginx-deployment
spec:
  replicas: 3
  selector:
    matchLabels:
      app: nginx
  template:
    metadata:
      labels:
        app: nginx
    spec:
      containers:
        - name: nginx
          image: nginx:1.22.1
          ports:
            - containerPort: 80
