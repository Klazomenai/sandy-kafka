# Build

Follows up from [sandy-zookeeper/README.md](https://github.com/Klazomenai/sandy-zookeeper)

 - Use Docker from within Minikube
```sh
eval $(minikube docker-env)
```

 - Build new Centos Docker image from the Dockerfile in thie repo
```sh
docker build . --tag=registry:5000/kafka:latest
```

 - Push newly build image to local Docker registry
```sh
docker push registry:5000/kafka:latest
```

 - Build new image on cluster
```sh
kubectl create -f kafka.yaml
```
