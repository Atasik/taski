# Taski
Приложение для планирования своих задач.

# Запуск Docker
```
docker compose up -d
```
либо
```
docker-compose up -d
```

# Запуск Kubernetes

```
kubectl apply -f namespace.yaml         
kubectl apply -f backend-deployment.yaml
kubectl apply -f frontend-deployment.yaml
kubectl apply -f backend-service.yaml
kubectl apply -f frontend-service.yaml
```

Для тестирования локально нужно сделать port-forwarding:

```
kubectl port-forward svc/taski-frontend 3000:80 -n taski 
kubectl port-forward svc/taski-backend 8080:8080 -n taski
```