# Lakehouse

## Installing on kubernetes

* Installing in default namespace
```bash
kubectl apply -f https://raw.githubusercontent.com/vikrantcue/lakehouse-templates/main/zeppelin-server.yaml 
```

* Installing in specific namespace
```bash
kubectl create namespace <Namespace> # Create a namespace if it does not exist. You can skip it if you want to install in an existing namespace
kubectl apply -f https://raw.githubusercontent.com/vikrantcue/lakehouse-templates/main/zeppelin-server.yaml -n <Namespace>
```
