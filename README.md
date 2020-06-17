#KUB-030 - Kubernetes Basics - Kumulus Technologies

From https://learn.kumul.us/kub-030

These are the notes and files needed for the Kumulus Technologies Kuberenets Basics class.  Here you will find a pod, deployment, and service description for a simple container service.

## Guestbook

A more complete example from the Kubernetes examples (https://github.com/kubernetes/examples), here we have the all-in-one version of a simple multi-pod scalealbe service including both a front end app and a backend database service (buitl from a distributed redis service):

Deploy with:

```
kubectl apply -f guestbook-all-in-one.yaml
```

If you don't have access to a LoadBalancer service (most test enviornments don't), you can simply port forward to the cluster:

```
kubectl port-forward svc/frontend 8080:80
```

And then point a browser to `https://localhost:8080`

