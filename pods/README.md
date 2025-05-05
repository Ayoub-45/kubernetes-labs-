# Kubernetes Pod Status

![Kubernetes Pod Screenshot](Screenshot%20from%202025-05-05%2008-39-56.png)

## Screenshot Description

The provided screenshot shows the output of the command:

```bash
kubectl get pods
```

This command is run from a terminal on a system named `ayoub@ayoub-Inspiron-3593`. It is used to list all running pods in the current Kubernetes namespace (usually `default`, unless otherwise specified).

## Pod Details

| Name  | Ready | Status  | Restarts       | Age |
|-------|-------|---------|----------------|-----|
| nginx | 1/1   | Running | 1 (91 minutes ago) | 98m |

### Breakdown:

- **NAME:** `nginx` — The name of the running pod.
- **READY:** `1/1` — One container is defined in the pod, and it is ready.
- **STATUS:** `Running` — The pod is currently active and operational.
- **RESTARTS:** `1 (91m ago)` — The container has restarted once, approximately 91 minutes ago. This may indicate a past crash or a manual restart.
- **AGE:** `98m` — The pod has been running for 98 minutes since it was first created.

## Notes

- This `nginx` pod is likely running a simple NGINX container, often used for basic web serving or as a placeholder during Kubernetes learning or development.
- The restart could indicate a transient issue shortly after pod creation.

## Prerequisites to Reproduce

To see a similar output on your machine:

1. Ensure you have a running Kubernetes cluster (e.g., Minikube or kind).
2. Deploy an NGINX pod:

   ```bash
   kubectl run nginx --image=nginx
   ```

3. Check pod status with:

   ```bash
   kubectl get pods
   ```
