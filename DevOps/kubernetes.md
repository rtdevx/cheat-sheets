# Kubernetes Cheat-Sheet

Command | Explanation
--------|-------------
`kubectl get nodes` | List all nodes in the cluster.
`kubectl get pods` | List all pods in the default namespace.
`kubectl get pods -n my-namespace` | List all pods in a specific namespace.
`kubectl get pods -o jsonpath={.items[*].metadata.name}` | List the names of all pods using jsonpath. 
`kubectl describe node my-node` | Detailed information about a specific node.
`kubectl describe pod my-pod` | Detailed information about a specific pod.
`kubectl logs my-pod` | Print the logs for a specific pod.
`kubectl exec my-pod -- date` | Execute a command in a specific pod (e.g., print current date).
`kubectl run my-pod --image=my-image` | Run a specific image in a new pod.
`kubectl delete pod my-pod` | Delete a specific pod.
`kubectl create -f my-config.yaml` | Create resources defined in a specific YAML file.
`kubectl apply -f my-config.yaml` | Apply changes to resources defined in a specific YAML file.
`kubectl delete -f my-config.yaml` | Delete resources defined in a specific YAML file.
`kubectl get services` | List all services in the default namespace.
`kubectl get services -n my-namespace` | List all services in a specific namespace.
`kubectl get deployments` | List all deployments in the default namespace.
`kubectl get deployments -n my-namespace` | List all deployments in a specific namespace.
`kubectl scale --replicas=3 deployment/my-deployment` | Scale a deployment to 3 replicas.
`kubectl rollout status deployment/my-deployment` | Check the rollout status of a specific deployment.
`kubectl rollout undo deployment/my-deployment` | Roll back the last update to a specific deployment.
