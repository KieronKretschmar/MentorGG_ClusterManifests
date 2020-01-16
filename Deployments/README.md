# Deployments

## MentorInterface

### Requirements:
- IngressController
- Certificate Manager

### Deployment:

1. Deploy the Ingress and Issuer.

    ```shell
    $ kubectl apply Ingress/api.mentor.gg/
    ```

2. Deploy the MySQL Helm Chart.

    ```shell
    $ helm install users -f MySQL/users/users-config.yml bitnami/mysql
    ```

    [Source](MySQL/README.md)

3. Deploy the container

    ```shell
    $ kubectl apply MentorServiceManifests/MentorInterface/<VERSION>.yml
    ```

