# HTTPie Debug Container

>  HTTPie—aitch-tee-tee-pie—is a command line HTTP client with an intuitive UI, JSON support, syntax highlighting, wget-like downloads, plugins, and more. 

- https://httpie.org/


## Deploy the HTTPie Pod

If the pod is not already deployed, run the following:

```shell
$ kubectl apply -f httpie.yml
```

## Attach an interactive shell


```shell
$ kubectl exec -ti httpie-debug -- /bin/sh

```

## Test an endpoint

```shell
/ # http mentor-interface/identity/76561198004197138
```


# Curl Debug Container

## Deploy

```shell
$ kubectl apply -f curl.yml
```

## Attach

```shell
$ kubectl exec -ti curl-debug -- /bin/sh
```

