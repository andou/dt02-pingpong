# Docker PingPong Playground

## Basic

### Run in attached mode

```
docker compose up
```

### Run in detached mode

```
docker compose up -d
```

### Put services down

```
docker compose down
```

## Swarm Mode

### Init the swarm

```
docker swarm init
```

### Deploy the stack

```
docker stack deploy --compose-file docker-stack.yml pingpong
```

Head to [http://localhost:8080/](http://localhost:8080/) for the visualizer, [http://localhost:8081/](http://localhost:8081/) for the ping and [http://localhost:8082/](http://localhost:8082/) for the pong

### Remove the stack

```
docker stack remove pingpong
```

### Leave the swarm

```
docker swarm leave --force
```

## Kubernetes

### Start minikube

```
minikube start
```

### Create namespace, deployments and services

```
kubectl create -f k8s-specifications/
```

### Remove namespace, deployments and services

```
kubectl delete -f k8s-specifications/
```

### Stop minikube

```
minikube stop
```
