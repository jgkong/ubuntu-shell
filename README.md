# debug-shell

Alpine and Ubuntu based image, to test K8s cluster internally.

## Included packages
* Alpine: busybox-extras bash curl tmux openssl
* Ubuntu: busybox curl tmux

## Usage

### Onetime run
```
kubectl run shell --rm -it --image=jgkong/debug-shell --restart=Never -- bash
```

### Longer lifecycle shell
```
kubectl run shell --image=jgkong/debug-shell --restart=Never
kubectl exec -it shell bash
kubectl delete pod shell
```
