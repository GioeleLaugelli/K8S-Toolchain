# Toolchain

### Eseguita con minikube

### Creare il nodo
minikube start --memory 6000 --cpus 4 --disk-size 50GB

### Abilitare i pacchetti utili per lo scopo(Dashboard e servizi) 
minikube addons enable dashboard
minikube addons enable metrics-server
minikube addons enable ingress 
minikube addons enable helm-tiller 

### Installazione di Jenkins
kubectl apply -f https://raw.githubusercontent.com/GioeleLaugelli/Toolchain-Single/main/namespace-jenkins.yaml
kubectl apply -f https://raw.githubusercontent.com/GioeleLaugelli/Toolchain-Single/main/volume-jenkins.yaml
kubectl apply -f https://raw.githubusercontent.com/GioeleLaugelli/Toolchain-Single/main/deployment-jenkins.yaml
kubectl apply -f https://raw.githubusercontent.com/GioeleLaugelli/Toolchain-Single/main/service-account-jenkins.yaml
kubectl apply -f https://raw.githubusercontent.com/GioeleLaugelli/Toolchain-Single/main/service-jenkins.yaml
