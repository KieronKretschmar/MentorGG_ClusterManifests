# Monitoring Ingress Authentication

This README applies to `monitoring.mentor.gg`

## Reading

- https://kubernetes.github.io/ingress-nginx/examples/auth/basic/

## Create Credentials


1. Create a file called `auth` with a user called `team`

    ```shell
    $ htpasswd -c auth team
    ```

    Enter in the new password.

2. Create the Kubernetes Secret

    The Monitoring Ingress expects a secret called `monitoring-ingress-auth`, so let's create one in the namespace `elastic-system`.

    ```shell
    $ kubectl create secret generic monitoring-ingress-auth --from-file=auth --namespace elastic-system
    ```

3. Remove the `auth` file







