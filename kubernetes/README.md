# Services

## Expose service usuarios

```$bash
kubectl expose deployment msvc-usuarios --port=8001 --type=LoadBalancer
```

## Expose service mysql

```$bash
kubectl expose deployment mysql --port=3306 --type=ClusterIP
```

## Url crash

```$bash
locahost:8001/crash
```

## Scale msvc-usuarios

```$bash
kubectl scale deployment msvc-usuarios --replicas=3
```

## delete

```$bash
kubectl delete service mysql
kubectl delete service msvc-usuarios
kubectl delete service postgres
kubectl delete service msvc-cursos
kubectl delete deployment mysql
kubectl delete deployment msvc-usuarios
kubectl delete deployment postgres
kubectl delete deployment msvc-cursos

O

kubectl delete -f deployment-mysql.yaml
kubectl delete -f deployment-msvc-usuarios.yaml
kubectl delete -f service-mysql.yaml
kubectl delete -f service-msvc-usuarios.yaml
kubectl delete -f deployment-postgres.yaml
kubectl delete -f deployment-msvc-cursos.yaml
kubectl delete -f service-postgres.yaml
kubectl delete -f service-msvc-cursos.yaml
```
