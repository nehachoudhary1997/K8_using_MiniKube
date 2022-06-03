# K8_using_MiniKube
Learn Kubernetes using MiniKube , Single Node Cluster

### to run cluster on minikube using docker
$ minikube start --driver=docker
$ minikube status|pause|stop
#### delete all clusters
$ minikube delete --all  
#### to run and delete container on cluster > pod auto created
$ kubectl run ng --image nginx
$ kubectl delete pod ng 

### to create pod 
$ kubectl create -f pod_defination.yml
