# Prometheus

## Source:

- Helm Chart: https://github.com/helm/charts/tree/master/stable/prometheus-operator

## Deploy:

```shell
$ helm install prometheus -f values.yml stable/prometheus-operator --namespace prometheus
```

# Upgrade 

```shell
$ helm upgrade prometheus -f values.yml stable/prometheus-operator --namespace prometheus
```

## Grafana Config

### Dashboards

Import the following Grafana dashboards

- Nginx `9614`, `10187`
- Redis `11835`
- RabbitMQ `10991`




