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


## Removing RabbitMQ (Clearing all Data)

First uninstall the chart

```shell
$ helm uninstall rabbitmq
```

Then, remove the Persistent Volume Claim (`pvc`)

```shell
$ kubectl delete pvc data-rabbitmq-0
```

Confirm the removal by checking for the existence of a Persistent Volume

```shell
$ kubectl get pv
```

## Testing Namespace

Append `-n testing` to all commands to make changes to the `testing` namespace.
