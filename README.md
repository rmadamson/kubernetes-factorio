# kubernetes-factorio

```
cat clusterio-client.yaml | sed 's/111/222/' > clusterio-client-222.yaml
```

```
for i in $(seq 1 9); do cat clusterio-client.yaml | sed 's/c5a64c18fd72138818648632ae7574//' | sed 's/111/'$i$i$i'/' > clusterio-client-$i$i$i.yaml; done
```

```
for i in $(seq 1 9); do kubectl create -f clusterio-client-$i$i$i.yaml; done 
for i in $(seq 1 9); do kubectl delete -f clusterio-client-$i$i$i$i.yaml; done
```
