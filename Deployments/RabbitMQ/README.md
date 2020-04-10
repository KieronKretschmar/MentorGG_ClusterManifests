# RabbitMQ

## Sources

- https://github.com/bitnami/charts/tree/master/bitnami/rabbitmq
- https://github.com/rabbitmq/rabbitmq-server/blob/master/docs/rabbitmq.conf.example

## Deployment

```shell
$ helm install rabbitmq -f values.yml bitnami/rabbitmq
```

## Upgrade

```shell
$ helm upgrade rabbitmq -f values.yml bitnami/rabbitmq
```

## Debugging

Port-forward `15672` to your localmachine for the Web UI.

```shell
$ kubectl port-forward rabbitmq-0 80:15672
```

## Notes

- When adjusting the resources, take care to adjust the `total_memory_available_override_value` configuration value.
