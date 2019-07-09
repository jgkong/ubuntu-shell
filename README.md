# ubuntu-shell

Ubuntu based image, to test K8s cluster internally.

Included packages: command-not-found net-tools vim iputils-ping telnet dnsutils screen curl wget bash-completion

## Usage

### Onetime run
```
kubectl run shell --rm -it --image=jgkong/ubuntu-shell --restart=Never -- bash
```

### Longer lifecycle shell
```
kubectl run shell --image=jgkong/ubuntu-shell --restart=Never
kubectl exec -it $(kubectl get pods -l run=shell -o jsonpath='{.items[0].metadata.name}') bash
```
