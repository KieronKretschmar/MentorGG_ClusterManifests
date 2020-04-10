# Redis

## Sources

- https://github.com/bitnami/charts/tree/master/bitnami/redis

## Deployment

```shell
$ ./<SERVICE>.helm
```

## Connecting to a instance of Redis

1. Retrieve the password secret.

    ```yaml
    - name: REDIS_PASSWORD
      valueFrom:
          secretKeyRef:
              name: match-data-sets-redis
              key: redis-password
    ```

2. Build the connection string.

    ```yaml
    - name: REDIS_URI
      value: "match-data-sets-redis-master:6379,password=$(REDIS_PASSWORD)"
    ```

3. Optionaly, append required arguments to the connection string, such as `syncTimeout=60000`


## Removing a Redis instance (Clearing all Data)

First uninstall the helm chart.

```shell
$ helm uninstall match-data-sets
```

Then if present, remove the Persistent Volume Claim (`pvc`).

```shell
$ kubectl delete pvc data-match-data-sets-redis
```

Confirm the removal is complete by checking the Persistent Volumes.
```shell
$ kubectl get pv
```

