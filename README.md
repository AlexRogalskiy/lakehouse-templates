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

## Zeppelin UI
Once the pod is running, run the following command to port forward zeppelin UI
```bash
kubectl port-forward services/zeppelin-server 8080:80 -n <namespace>
```

## Lakehouse UI
```bash
kubectl port-forward services/lakehouse 8000:80 -n <namespace>
```
