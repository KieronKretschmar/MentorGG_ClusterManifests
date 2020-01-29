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

3. Initialize the Database
    
    First, port-forward the MySQL master container to your local machine.

    The following commmand forwards the port `3306` from the pod to `3307` of your local workstation.

    ```shell
    kubectl port-forward <POD> 3307:3306
    ```

    Second, navigate to the directory of the project and run the migration.

    ```shell
    $ MYSQL_CONNECTIONSTRING="server=localhost;port=3307;userid=<USER>;password=<PASSWORD>;database=<DATABASE>;" \
    dotnet ef database update --project ../Database --startup-project .
    ```

3. Deploy the container

    ```shell
    $ kubectl apply MentorServiceManifests/MentorInterface/<VERSION>.yml
    ```

