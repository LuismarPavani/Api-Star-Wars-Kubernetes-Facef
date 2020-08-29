# Kubernetes Facef 2020
Exercício do curso de Kubernetes da Facef.


# Docker

Modo de uso

## build pelo docker
 ```
docker build -f Dockerfile -t luismar/api_star_wars:0.0.1 .
 ```

## login para o push
 ```
docker login -u luismar
 ```

## push no docker hub
 ```
docker push luismar/api_star_wars:0.0.1
 ```

# API do Star Wars no Cluster

Modo de uso

## deployment
 ```
 kubectl apply -f api-star-wars-deployment.yaml
 ```
 
## service
 ```
 kubectl apply -f api-star-wars-service.yaml
 ```

## expondo a porta HTTPS
 ```
 kubectl port-forward service/api-star-wars-service 9000:9000
 ```
