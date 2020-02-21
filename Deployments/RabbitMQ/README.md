# RabbitMQ

# Sources

- https://github.com/bitnami/charts/tree/master/upstreamed/rabbitmq

# Deployment

```shell
$ helm install rabbitmq -f values.yml stable/rabbitmq
```

# Debugging

Port-forward `15672` to your localmachine for the Web UI.

```shell
$ kubectl port-forward rabbitmq-0 80:15672
```
