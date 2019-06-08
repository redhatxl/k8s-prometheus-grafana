# k8s-prometheus-grafana

[Kubernetes+Prometheus+Grafana部署笔记](https://blog.51cto.com/kaliarch/2160569)


# grafana 
admin/admin

# grafana nonPersistence
```
kubectl create -f k8s-prometheus-grafana/prometheus-grafana/grafana/
```

# grafana persistence
```
kubectl create -f k8s-prometheus-grafana/prometheus-grafana/grafana/
kubectl apply -f k8s-prometheus-grafana/prometheus-grafana/grafana/persistence/
```


# heapster
```
kubectl create -f metrics-server  
kubectl create -f heapster-influxdb-grafana

[root@master k8s-prometheus-grafana]# kubectl top node
NAME     CPU(cores)   CPU%   MEMORY(bytes)   MEMORY%   
master   150m         7%     1078Mi          62%  
```

