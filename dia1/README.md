### Pasos del primer día

1. Crear pod `01-pod.yaml`
```shell
kubectl create -f 01-pod.yaml
```
2. Borrar pod `01-pod.yaml`
```shell
kubectl delete -f 01-pod.yaml
```
3. Crear pod `02-pod.yaml`
```shell
kubectl create -f 02-pod.yaml
```
4. Borrar pod `02-pod.yaml`
```shell
kubectl delete -f 02-pod.yaml
```
5. Crear primer deployment, usar archivo `03-deploy.yaml`
```shell
kubectl apply -f 03-deploy.yaml
```
6. escalar deployment
```shell
kubectl scale deployment/gpod-deploy --replicas=<numero de replicas>
```

```shell
kubectl get rs
```

```shell
kubectl get pods -o wide
```


7. Crear servicio ClusterIP `04-svc-cluster.yaml`
```shell
kubectl apply -f 04-svc-clusterip.yaml
```

```shell
kubectl get services
```

```shell
kubectl get svc 
```

```shell
kubectl describe svc/gpod 
```


8. entrar al container y comunicar con el puerto
```shell
kubectl exec -ti gdeploy-75b9d6844d-grm7v sh
```

```shell
wget -qO- gpod:8080
``` 

9. Crear servicio NodePort `04-svc-nodeport.yaml`

```shell
kubectl apply -f 04-svc-nodeport.yaml
```
```shell
kubectl get svc 
```

```shell
kubectl describe svc/gpod-svc-np
```

10. revisar logs y acceder al servicio
```shell
curl http://localhost:<port>/
```

11. Crear servicio LoadBalancer `04-svc-loadbalancer.yaml`
```shell
kubectl apply -f 04-svc-loadbalancer.yaml
```
```shell
kubectl get svc 
```

```shell
kubectl describe svc/gpod-svc-lb
```
12. Revisar loadBalancer
```shell
curl http://localhost/
```
