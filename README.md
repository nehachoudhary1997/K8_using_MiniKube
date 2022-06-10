# K8_using_MiniKube
Learn Kubernetes using MiniKube , Single Node Cluster
</br>

# Deployment creates Replicaset which in turn creates Pod.</br>
# Services creates communication between end users and application(Pod) using NodePort . Also , acts as a LoadBalancer.</br>

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
<i> View RS, Rc , pods</i></br>
$ kubectl get replicationcontroller </br>
$ kubectl get replicaset</br>
$ kubectl get pods</br>
</br>

#### create deployments- update and rollback
$ kubectl create -f deployment-defination.yml </br>
$ kubectl get deployments </br>
$ kubectl describe deployment deployment-name </br>

#### update
$ kubectl apply -f deployment-defination.yaml</br>
$ kubectl set image deployment/DEPLOYMENT-name nginx=nginx:1.9.1 </br>
<i> does not update config file </i>
</br>
#### rollback
$ kubectl rollout status deployment/DNAME </br>
$ kubectl rollout history deployment/DNAME </br>
$ kubectl rollout undo deplloyment/DNAME </br>
  
### Service
$ kubectl create -f service-def.yml </br>
$ kubectl get services </br>
