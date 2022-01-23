# kubernates-Commands
<h3>install hyperhit and minikube</h3>
brew update
brew install hyperkit
brew install minikube
kubectl
minikube

<h3>create minikube cluster</h3>
minikube start --vm-driver=hyperkit
kubectl get nodes
minikube status
kubectl version

<h3>delete cluster and restart in debug mode</h3>
minikube delete
minikube start --vm-driver=hyperkit --v=7 --alsologtostderr
minikube status

<h3>kubectl commands</h3>
kubectl get nodes
kubectl get pod
kubectl get services
kubectl create deployment nginx-depl --image=nginx
kubectl get deployment
kubectl get replicaset
kubectl edit deployment nginx-depl

<h3>debugging</h3>
kubectl logs {pod-name}
kubectl exec -it {pod-name} -- bin/bash

<h3>create mongo deployment</h3>
kubectl create deployment mongo-depl --image=mongo
kubectl logs mongo-depl-{pod-name}
kubectl describe pod mongo-depl-{pod-name}

<h3>delete deplyoment</h3>
kubectl delete deployment mongo-depl
kubectl delete deployment nginx-depl

<h3>create or edit config file</h3>
vim nginx-deployment.yaml
kubectl apply -f nginx-deployment.yaml
kubectl get pod
kubectl get deployment

<h3>delete with config</h3>
kubectl delete -f nginx-deployment.yaml
#Metrics
kubectl top The kubectl top command returns current CPU and memory usage for a cluster’s pods or nodes, or for a particular pod or node if specified.
