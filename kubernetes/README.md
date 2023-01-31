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
