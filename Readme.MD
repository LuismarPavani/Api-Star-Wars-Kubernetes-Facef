# Kubernetes Facef 2020
Exercício do curso de Kubernetes da Facef.


## Docker Image

Modo de uso

v0.0.1
```
docker run -p 8080:8080 luismar/api_star_wars:0.0.1
```

v0.0.2
```
docker run -p 8080:8080 luismar/api_star_wars:0.0.2
```

## Lista de comandos usados

```
kubeclt get nodes -o wide - lista os nodes com mais informacoes
kubeclt get pods -o wide - lista os pods com mais informacoes
kubectl get pods -w - lista os pods e acompanha todas as alteracoes
kubectl set image deployment hello-api hello-api=luismar/api_star_wars:0.0.2 - troca a imagem e versão do deployment
kubectl logs -f pods <pod_id> - mostra os logs do pod e acompanha novas saidas de logs
kubectl logs -p <pod_id> - mostra os logs antes do restart do pod/container
kubectl describe pod <pod_id> - exibe todas as informacoes de um pod
kubectl top pod - exibe os recurso utilizado.

kubectl apply -f file.yaml - aplica todos os recursos descritos no arquivo
kubectl diff -f file.yaml - exibe as diferenças entre o cluster e o arquivo
kubectl delete -f file.yaml - apaga todos os recursos descritos no arquivo

kubectl autoscale deployment api-star-wars-deployment --min 1 --max 10 --cpu-percent 50 - cria um autoscale para o deployment


microk8s enable metrics-server - habilita o metric-server
minikube addons enable metrics-server - habilita o metric-server


kubectl run -it --rm load-generator --image=busybox /bin/sh
while true; do wget -q -O- http://api-star-wars-service:8080; done

```


