# MySQL Deployment

# Source 

- Image: https://github.com/bitnami/bitnami-docker-mysql
- Helm Chart: https://github.com/bitnami/charts/tree/master/bitnami/mysql

# Deployment

```shell
$ helm install <deployment name> -f <service>-config.yml bitnami/mysql
```

# Upgrade Example 

1. Obtain the password as described on the 'Administrator credentials' section and set the 'root.password' parameter as shown below:

      ROOT_PASSWORD=$(kubectl get secret --namespace default demo-central-mysql -o jsonpath="{.data.mysql-root-password}" | base64 --decode)
      helm upgrade demo-central bitnami/mysql --set root.password=$ROOT_PASSWORD
