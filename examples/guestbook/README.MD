##Run the following commands to start a guestbook service locally, a validate=false flag might need to be used in some areas.

```
kubectl create -f redis-master-controller.yaml

kubectl create -f redis-master-service.yaml

kubectl create -f redis-slave-controller.yaml

kubectl create -f redis-slave-service.yaml

kubectl create -f frontend-controller.yaml

kubectl create -f frontend-service.yaml
```

##Cleanup and Removal

```
kubectl stop rc -l "name in (redis-master, redis-slave, frontend)"
kubectl delete service -l "name in (redis-master, redis-slave, frontend)"
```
