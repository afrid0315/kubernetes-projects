# kubernetes-commands

#### kubectl get pods -> to get pods
#### kubectl get deployments -> to get deployments
#### kubectl apply -f deployment -> to apply changes of deployment
#### kubectl scale deployment --replicas=0 redis-deployment -> to scale down to 0 replicas
#### kubectl scale deployment --replicas=1 redis-deployment -> to scale up to 1 replicas
#### kubectl get configmap -> to get configmap
#### kubectl edit deployment -> to edit existing deployment
#### kubectl get deploy -> to get deployments
#### kubectl get pods -w -> to watch the pods
#### kubectl get replicasets -> to get replicaset
#### kubectl logs <pod-name> -> to get logs of that pods
#### kubectl rollout history deployment redis-deployment -> to Check the rollout history to see if there were recent changes that might have caused the issue
#### kubectl describe pod <podname> -> to get details of particular pods
#### kubectl exec -it <podname> -c <containername> -- sh  -> to enter into that particular pods container and work in it.
#### kubectl create namespace <my-namespace> -> to create a namespace
#### kubectl get pods --namespace=<my-namespace> -> to get pods which are of particular namespace.
#### kubectl get namespace -> to get namespace
#### kubectl get svc -> to get service
#### kubectl get svc --namespace=<my-namespace> -> to get services which are of particular namespace.
