# Services

## Expose service usuarios in imperative mode

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

## UP

```$bash
kubectl apply -f secret.yaml
kubectl apply -f configmap.yaml

kubectl apply -f mysql-pv.yaml
kubectl apply -f mysql-pvc.yaml

kubectl apply -f deployment-mysql.yaml
kubectl apply -f service-mysql.yaml

kubectl apply -f deployment-msvc-usuarios.yaml
kubectl apply -f service-msvc-usuarios.yaml

kubectl apply -f postgres-pv.yaml
kubectl apply -f postgres-pvc.yaml

kubectl apply -f deployment-postgres.yaml
kubectl apply -f service-postgres.yaml

kubectl apply -f deployment-msvc-cursos.yaml
kubectl apply -f service-msvc-cursos.yaml
```

## delete

```$bash
kubectl delete deployment mysql
kubectl delete service mysql
kubectl delete deployment msvc-usuarios
kubectl delete service msvc-usuarios
kubectl delete pvc mysql-pvc
kubectl delete pv mysql-pv

kubectl delete deployment postgres
kubectl delete service postgres
kubectl delete deployment msvc-cursos
kubectl delete service msvc-cursos
kubectl delete pvc postgres-pvc
kubectl delete pv postgres-pv

kubectl delete secret msvc-usuarios
kubectl delete secret msvc-cursos

kubectl delete configmap msvc-usuarios
kubectl delete configmap msvc-cursos

O

kubectl delete -f deployment-mysql.yaml
kubectl delete -f deployment-msvc-usuarios.yaml
kubectl delete -f deployment-postgres.yaml
kubectl delete -f deployment-msvc-cursos.yaml
kubectl delete -f service-mysql.yaml
kubectl delete -f service-msvc-usuarios.yaml
kubectl delete -f service-postgres.yaml
kubectl delete -f service-msvc-cursos.yaml
kubectl delete -f postgres-pvc.yaml
kubectl delete -f mysql-pvc.yaml
kubectl delete -f postgres-pv.yaml
kubectl delete -f mysql-pv.yaml
kubectl delete -f secrets.yaml
kubectl delete -f configmap.yaml
```
