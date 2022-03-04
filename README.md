# Argo hosted Jupyter Notebook

This deployment launches a jupyter notebook on the Argo cluster until the user deletes it.

## Launch

Submit the job to your provided argo cluster like the following example:

```
argo -n argo submit argo_jupyter.yaml
# Port forward from the cluster
kubectl -n argo port-forward pod/jupyter 8888:8888
```

If you don't have local access to kubectl use SSH port forwarding at this point.
