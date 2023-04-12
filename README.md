# workshop-k8s

## K3d

https://k3d.io/v5.4.9/

### Requisitos

- Docker
> Note: k3d v5.x.x requires at least Docker v20.10.5 (runc >= v1.0.0-rc93) to work properly (see #807)
- [kubectl](https://kubernetes.io/docs/tasks/tools/#kubectl) to interact with the Kubernetes cluster


### Instalação

#### kubectl

curl.exe -LO "https://dl.k8s.io/release/v1.26.0/bin/windows/amd64/kubectl.exe" ou 
choco install kubernetes-cli

#### k3d

```sh
wget -q -O - https://raw.githubusercontent.com/k3d-io/k3d/main/install.sh | bash
```

ou

```sh
curl -s https://raw.githubusercontent.com/k3d-io/k3d/main/install.sh | bash
```

### Gerenciando Clusters

#### Criando um Cluster

```sh
k3d cluster create mycluster
```

#### Criando um cluster com LoadBalancer

```sh
k3d cluster create --agents 1 --servers 1 -p "8080:30000@loadbalancer"
```
