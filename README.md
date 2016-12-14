### Create a deployment
`kubectl run hello-minikube --image=gcr.io/google_containers/echoserver:1.4 --port=8080`


### Create a service
`kubectl expose deployment hello-minikube --type=NodePort`


### List the pods
`kubectl get pod`


### List the service
`kubectl get service`


### Test the service
`curl $(minikube service hello-minikube --url)/health`


### List the ReplicaSets
`kubectl get rs`


### Scale the ReplicaSet
`kubectl scale deployments/hello-minikube --replicas=3`


### List the pods
`kubectl get pod`


### Test the service
`curl $(minikube service hello-minikube --url)/health3`


### Show the dashboard
`open $(minikube service kubernetes-dashboard --namespace=kube-system --url)`
