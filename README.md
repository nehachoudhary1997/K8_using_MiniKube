# K8_using_MiniKube
Learn Kubernetes using MiniKube , Single Node Cluster
</br>

### Run cluster on minikube using docker
$ minikube start --driver=docker </br>
$ minikube start|status|pause|stop
</br>

#### Delete all clusters
$ minikube delete --all
</br>

#### Run and delete container on cluster > pod auto created, edit pod 
$ kubectl run ng --image nginx </br>
$ kubectl delete pod ng 
</br>
$ kubectl edit pod ng
</br><i> This opens auto created definationfile for pom> edit this and save , updated pod created </i>

### to create pod 
$ kubectl create -f pod_defination.yml

### create ReplicationController and ReplicaSet
$ kubectl create -f rc_defination.yml </br>
$ kubectl create -f replicationset_defination.yml
</br>
</br>
<i> View RS, Rc , pods</i>
$ kubectl get replicationcontroller </br>
$ kubectl get replicaset</br>
$ kubectl get pods</br>
</br>
