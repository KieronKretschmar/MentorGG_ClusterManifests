# Prometheus

## Source:

- Helm Chart: https://github.com/helm/charts/tree/master/stable/prometheus-operator

## Deploy:

```shell
$ helm install prometheus -f values.yml stable/prometheus-operator --namespace monitoring
```

# Upgrade 

```shell
$ helm upgrade prometheus -f values.yml stable/prometheus-operator --namespace monitoring
```


