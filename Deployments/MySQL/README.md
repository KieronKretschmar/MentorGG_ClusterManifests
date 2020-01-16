# MySQL Deployment

# Source 

- Image: https://github.com/bitnami/bitnami-docker-mysql
- Helm Chart: https://github.com/bitnami/charts/tree/master/bitnami/mysql

# Deployment

```shell
$ helm install <deployment name> -f <service>-config.yml bitnami/mysql
```

# Upgrade 

```shell
$ helm upgrade <deployment name> -f <service>.yml  bitnami/mysql
```
