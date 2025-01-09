Here’s the **README** content that you can directly copy and paste into your GitHub repository’s `README.md` file.

```markdown
# Kubernetes Commands Guide

This repository provides a collection of basic Kubernetes commands that are essential for managing and interacting with Kubernetes clusters. Use these commands to deploy, monitor, and manage your applications in Kubernetes.

## **Prerequisites**

Before you begin using the Kubernetes commands, ensure you have the following:

- **kubectl** installed on your local machine.
- Access to a running **Kubernetes cluster** (either locally with Minikube, on a cloud provider like Azure/AWS/GCP, or on a managed Kubernetes service).

## **Common Kubernetes Commands**

### 1. **Get Cluster Information**
   - Get the cluster information:
     ```bash
     kubectl cluster-info
     ```

### 2. **Get Nodes**
   - View the nodes in your cluster:
     ```bash
     kubectl get nodes
     ```

### 3. **Get Pods**
   - List all pods in the default namespace:
     ```bash
     kubectl get pods
     ```
   - List all pods in a specific namespace:
     ```bash
     kubectl get pods -n <namespace>
     ```

### 4. **Get Deployments**
   - List all deployments in the current namespace:
     ```bash
     kubectl get deployments
     ```
   - List deployments in a specific namespace:
     ```bash
     kubectl get deployments -n <namespace>
     ```

### 5. **Get Services**
   - List all services in the current namespace:
     ```bash
     kubectl get services
     ```
   - List services in a specific namespace:
     ```bash
     kubectl get services -n <namespace>
     ```

### 6. **Get Namespaces**
   - List all namespaces in the cluster:
     ```bash
     kubectl get namespaces
     ```

### 7. **Get Logs of a Pod**
   - Get the logs of a specific pod:
     ```bash
     kubectl logs <pod-name>
     ```

### 8. **Apply a Configuration**
   - Apply a configuration file (YAML or JSON) to the cluster:
     ```bash
     kubectl apply -f <file-name>.yaml
     ```

### 9. **Create Resources**
   - Create resources from a YAML or JSON file:
     ```bash
     kubectl create -f <file-name>.yaml
     ```

### 10. **Delete Resources**
   - Delete a pod:
     ```bash
     kubectl delete pod <pod-name>
     ```
   - Delete a deployment:
     ```bash
     kubectl delete deployment <deployment-name>
     ```
   - Delete a service:
     ```bash
     kubectl delete service <service-name>
     ```

### 11. **Scale a Deployment**
   - Scale a deployment (increase/decrease the number of replicas):
     ```bash
     kubectl scale deployment <deployment-name> --replicas=<number-of-replicas>
     ```

### 12. **Expose a Pod or Deployment**
   - Expose a pod as a service:
     ```bash
     kubectl expose pod <pod-name> --port=<port> --name=<service-name>
     ```
   - Expose a deployment as a service:
     ```bash
     kubectl expose deployment <deployment-name> --port=<port> --name=<service-name>
     ```

### 13. **Exec into a Running Pod**
   - Access a running pod using a shell:
     ```bash
     kubectl exec -it <pod-name> -- /bin/bash
     ```
   - For a specific container in the pod:
     ```bash
     kubectl exec -it <pod-name> -c <container-name> -- /bin/bash
     ```

### 14. **Get Pod Details**
   - Describe a pod to see more details (e.g., logs, events, etc.):
     ```bash
     kubectl describe pod <pod-name>
     ```

### 15. **Get Cluster Resources**
   - View detailed information about the cluster's resources:
     ```bash
     kubectl top nodes
     kubectl top pods
     ```

### 16. **Check Resource Usage**
   - View CPU and memory usage of pods or nodes:
     ```bash
     kubectl top pod <pod-name>
     kubectl top node <node-name>
     ```

### 17. **Set an Environment Variable for a Pod/Deployment**
   - Set or update an environment variable in a pod or deployment:
     ```bash
     kubectl set env deployment/<deployment-name> <env-name>=<value>
     ```

### 18. **Rolling Update a Deployment**
   - Perform a rolling update of a deployment:
     ```bash
     kubectl rollout restart deployment <deployment-name>
     ```

### 19. **Rollback a Deployment**
   - Rollback to a previous version of a deployment:
     ```bash
     kubectl rollout undo deployment <deployment-name>
     ```

### 20. **Forward a Port**
   - Forward a local port to a pod's port (useful for debugging):
     ```bash
     kubectl port-forward pod/<pod-name> <local-port>:<pod-port>
     ```

### 21. **Get ConfigMaps**
   - List all ConfigMaps in the cluster:
     ```bash
     kubectl get configmaps
     ```

### 22. **Get Secrets**
   - List all secrets in the cluster:
     ```bash
     kubectl get secrets
     ```

### 23. **Get Ingress**
   - List all ingress resources:
     ```bash
     kubectl get ingress
     ```

### 24. **Namespace Operations**
   - Create a new namespace:
     ```bash
     kubectl create namespace <namespace-name>
     ```
   - Switch between namespaces:
     ```bash
     kubectl config set-context --current --namespace=<namespace-name>
     ```

## **Useful Tips**
- **kubectl explain**: Get detailed information about the resources, such as a pod or deployment.
  ```bash
  kubectl explain pod
  kubectl explain deployment
  ```

- **Context Switching**: Switch between clusters or namespaces easily:
  ```bash
  kubectl config use-context <context-name>
  ```

## **Further Reading**
For more detailed information, you can always check the official Kubernetes documentation:
- [Kubernetes Documentation](https://kubernetes.io/docs/)

---

### How to Contribute:
- Fork this repository, add new commands or edits, and submit a pull request.
- Any improvements are welcome!
```

---

You can now copy this entire content into your `README.md` file on GitHub. This will give you a comprehensive guide to common Kubernetes commands with brief descriptions, ready for your repository!
