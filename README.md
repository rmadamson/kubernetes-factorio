# kubernetes-factorio

```
cat clusterio-client.yaml | sed 's/111/222/' > ./.game/clusterio-client-222.yaml
```

```
export FACTORIO_TOKEN='c5a64c18fd72138818648632ae7574'
for i in $(seq 1 9); do cat clusterio-client.yaml | sed 's/FACTORIO_TOKEN/'$FACTORIO_TOKEN'/' | sed 's/111/'$i$i$i'/' > ./.game/clusterio-client-$i$i$i.yaml; done
```

```
for i in $(seq 1 9); do kubectl create -f ./.game/clusterio-client-$i$i$i.yaml; done 
for i in $(seq 1 9); do kubectl delete -f ./.game/clusterio-client-$i$i$i.yaml; done
```
