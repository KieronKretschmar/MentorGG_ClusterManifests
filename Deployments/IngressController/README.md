
~# Ingress

## Source:

- Helm Chart: https://github.com/bitnami/charts/tree/master/bitnami/nginx-ingress-controller

- https://cert-manager.io/docs/installation/kubernetes/

## Deployment

```shell
$ helm install ingress -f values.yml -n ingress-controller bitnami/nginx-ingress-controller
```

## Upgrade

```shell
$ helm upgrade ingress -f values.yml -n ingress-controller  bitnami/nginx-ingress-controller
```
