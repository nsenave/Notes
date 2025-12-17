# Kubernetes

Architecture Kubernetes :

- https://phoenixnap.com/kb/understanding-kubernetes-architecture-diagrams
- https://www.educative.io/answers/the-kubernetes-architecture-simplified

Autres articles phoenixnap.com :

- API Server: https://phoenixnap.com/glossary/api-server
- Kubectl cheat sheet: https://phoenixnap.com/kb/kubectl-commands-cheat-sheet
- What is Kubernetes: https://phoenixnap.com/kb/what-is-kubernetes

Log rotation in Kubernetes:
- https://kubernetes.io/docs/concepts/cluster-administration/logging/#log-rotation

Which Linux OS runs on pod
```bash
kubectl exec -it <pod> -- /bin/bash -c "cat /etc/os-release;uname -r"
```

Show current namespace
- https://stackoverflow.com/questions/55853977/how-to-get-the-current-namespace-of-current-context-using-kubectl
  - https://stackoverflow.com/a/58636574
```
kubectl config view | grep namespace
```
