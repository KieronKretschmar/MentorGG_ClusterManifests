# RabbitMQ

# Sources

- https://github.com/bitnami/charts/tree/master/bitnami/rabbitmq

# Deployment

```shell
$ helm install rabbitmq -f values.yml bitnami/rabbitmq
```

# Debugging

Port-forward `15672` to your localmachine for the Web UI.

```shell
$ kubectl port-forward rabbitmq-0 80:15672
```
