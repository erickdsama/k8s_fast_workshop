# k8s_fast_workshop

## Indice


[DIA 1](dia1) Introudcción y practica en local

[DIA 2](dia1) DigitalOcean, primer proyecto(Explicación, deploy)

[DIA 3](dia1) Primer Proyecto(Volumenes, Nginx Ingress, cert-manager)

[DIA 4](dia1) primer proyecto (HPA, Locust)

## RECURSOS

instalar docker:

Ubuntu:
https://docs.docker.com/engine/install/ubuntu/

MacOS
https://docs.docker.com/desktop/mac/install/

WINDOWS
https://docs.docker.com/desktop/windows/install/

## ACTIVAR Kubernetes en docker-desktop
![](resources/settings-kubernetes.png)


### Comandos comunes para PODS 

+ crear un pod 

```shell
kubectl create -f <path_yaml_file>
```

+ eliminar un pod 

```shell
kubectl delete -f <path_yaml_file>
```

+ aplicar configuración a un pod

```shell
kubectl apply -f <path_yaml_file>
```

+ listar pods 

```shell 
kubectl get pods
```

+ listar pods con más información

```shell
kubectl get pods -o wide
```

+ describir información de un pod

```shell
kubectl describe pod/<POD_NAME>
```

+ describir información de un pod

```shell
kubectl describe pod/<POD_NAME>
```

### Comandos comunes para Deploys

+ Listar los deployments disponibles
```shell
kubectl get deployments
```

+ Listar los deployments disponibles
```shell
kubectl describe deployments/<deployment_name>
```
+ Listar los deployments disponibles
```shell
kubectl get replicaset
```
+ Escalar un deployment
```shell
kubectl scale deployment/<deployment_name> --replicas=<numero de replicas>
```

