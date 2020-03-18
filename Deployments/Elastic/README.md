# Elastic Stack

Cluster wide Logging and Metrics platform.

## Reading

- https://www.elastic.co/what-is/elk-stack
- https://www.linode.com/docs/kubernetes/how-to-deploy-the-elastic-stack-on-kubernetes/

## Requirements

1. Elastic Helm Repo

    ```shell
    $ helm repo add elastic https://helm.elastic.co
    ```

2. Kubernetes Namespace: `elastic-system`

    ```shell
    $ kubectl create ns elastic-system
    ```

## Elastic Search

- https://github.com/elastic/helm-charts/tree/master/elasticsearch

### Deployment

```shell
$ helm install elasticsearch -f elasticsearch-values.yml elastic/elasticsearch --namespace elastic-system 
```

## Filebeat

- https://github.com/elastic/helm-charts/tree/master/filebeat

### Deployment

```shell
$ helm install filebeat -f filebeat-values.yml elastic/filebeat --namespace elastic-system 
```

## Metricbeat

- https://github.com/elastic/helm-charts/tree/master/metricbeat

### Deployment

```shell
$ helm install metricbeat elastic/metricbeat --namespace elastic-system 
```

## Kibana

- https://github.com/elastic/helm-charts/tree/master/kibana

### Deployment

```shell
$ helm install kibana -f kibana-values.yml elastic/kibana --namespace elastic-system 
```
