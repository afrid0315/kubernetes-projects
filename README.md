# kubernetes-commands

https://kubernetes.io/docs/reference/generated/kubectl/kubectl-commands

https://github.com/kodekloudhub/certified-kubernetes-administrator-course?tab=readme-ov-file
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
#### kubectl create secret generic database --from-literal=MYSQL_ROOT_PASSWORD=ssdfgv --from-literal=MYSQL_DATABASE=cfghjjncd  -> to create secrets of key value pair in database.
#### kubectl cp /host/filepath <podname>:/containerpath -c <containername> -> to copy file from host to particular container.
#### kubectl create secret generic mysql-root-pass --from-literal=password=R00t  -> to create secrets of key value pair.
#### kubectl expose deployment <pod-name> --type=NodePort --port=80 --name=<service-name> -> creating nodeport service using command
#### k edit svc
#### kubectl get pod -o wide (-o=output)  -> more detail of pod
#### kubectl get deployment <deployment-name> -o yaml > deployment.yaml  -> to copy deployment file to deployment.yaml
#### kubectl scale --replicaset=6 -f replicaset.yml -> to scale or replace replica value
#### kubectl run nginx --image=nginx -> without yaml we can directly create pod using name and image
#### kubectl get pods --all-namespace (or) kubectl get pods -A -> these gives all pods present in different namespaces

## Generate POD Manifest YAML file (-o yaml). Don’t create it(–dry-run)

#### kubectl run nginx --image=nginx --dry-run=client -o yaml

## Create a deployment

#### kubectl create deployment --image=nginx nginx

## Generate Deployment YAML file (-o yaml). Don’t create it(–dry-run)

#### kubectl create deployment --image=nginx nginx --dry-run=client -o yaml

## Generate Deployment YAML file (-o yaml). Don’t create it(–dry-run) and save it to a file.

#### kubectl create deployment --image=nginx nginx --dry-run=client -o yaml > nginx-deployment.yaml

## Make necessary changes to the file (for example, adding more replicas) and then create the deployment.

#### kubectl create -f nginx-deployment.yaml

#### kubectl set image deployment nginx nginx=nginx:1.18 -> to update existing deployment image 

## Create a Service named redis-service of type ClusterIP to expose pod redis on port 6379

#### kubectl expose pod redis --port=6379 --name redis-service --dry-run=client -o yaml

## Create a Service named nginx of type NodePort to expose pod nginx’s port 80 on port 30080 on the nodes:

#### kubectl expose pod nginx --type=NodePort --port=80 --name=nginx-service --dry-run=client -o yaml
