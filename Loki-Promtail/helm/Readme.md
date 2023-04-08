## Loki-Stack Kurulumu
Loki Stack diger bilesenlerin kurulmasinida saglayabilir. Diger folderlardaki, Prometheus ve Grafana kurulumlarida bu stack altinda yapilabilir. 

Simdi tum bilesenlerin kurulumu yapilacak, storage olarak longhorn kullanilacak.


Download the values.yaml
```
helm show values grafana/loki-stack > values.yaml
```

```
helm install loki grafana/loki-stack --namespace loki-stack --values loki-stack-values.yaml
```

https://github.com/grafana/helm-charts/tree/main/charts/loki-stack 

Sadece Loki ve Promtail  kurmak icin 
```
helm install loki grafana/loki-stack --namespace=observability
```


Silmek icin 

```
helm uninstall loki  -n observability
```