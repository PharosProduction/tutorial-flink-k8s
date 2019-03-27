# Tutorial on How to Deploy Flink Cluster & Flink-exporter in Kubernetes Cluster

## You can find it in our Medium publication
[Pharos Production Medium Article](https://medium.com/pharos-production/how-to-deploy-flink-flink-exporter-in-kubernetes-cluster-48e24b440446).

Also you're warmely welcome to say hello to us
[Pharos Production - Blockchain and FinTech Software Development](https://pharosproduction.com)


## Flink session cluster on Kubernetes
A basic Flink session cluster deployment in Kubernetes has three components:

a Deployment/Job which runs the JobManager
a Deployment for a pool of TaskManagers
a Service exposing the JobManager’s REST and UI ports

## If using MiniKube please make sure to execute:

minikube ssh 'sudo ip link set docker0 promisc on'

before deploying a Flink cluster. Otherwise Flink components are not able to self reference themselves through a Kubernetes service.

## Deploy Flink session cluster on Kubernetes

kubectl apply -f flink




