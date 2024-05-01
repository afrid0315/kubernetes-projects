# kubernetes-couponsLinkForExamination

https://couponcause.com/stores/linux-foundation/?matchtype=e&device=c&network=g&creative=643034165747&keyword=linux%20foundation%20promo&targetid=kwd-332562668813&position=&adgroup=49768141332&locaton=9061552&locationint=&campaign=879582855&extention=&gclick=Cj0KCQjwiYOxBhC5ARIsAIvdH50USOjmICLMWOjWucnqmyfhrrviZTjExV753MSejQwhj5CvWf7qGwMaAvBsEALw_wcB&gad_source=1&gclid=Cj0KCQjwiYOxBhC5ARIsAIvdH50USOjmICLMWOjWucnqmyfhrrviZTjExV753MSejQwhj5CvWf7qGwMaAvBsEALw_wcB

# kubernetes-commands

https://www.kubernetes.dev/docs/onboarding/

https://kodekloud.com/courses/json-path-quiz/

https://kubernetes.io/docs/reference/generated/kubectl/kubectl-commands

https://github.com/kodekloudhub/certified-kubernetes-administrator-course?tab=readme-ov-file

https://github.com/kubernetes/community/blob/master/contributors/devel/sig-scheduling/scheduling_code_hierarchy_overview.md

https://kubernetes.io/blog/2017/03/advanced-scheduling-in-kubernetes/

https://jvns.ca/blog/2017/07/27/how-does-the-kubernetes-scheduler-work/

https://kubernetes.io/docs/tasks/administer-cluster/encrypt-data/

https://kubernetes.io/docs/concepts/configuration/secret/#protections

https://kubernetes.io/docs/tasks/administer-cluster/configure-upgrade-etcd/#backing-up-an-etcd-cluster

https://github.com/etcd-io/website/blob/main/content/en/docs/v3.5/op-guide/recovery.md

https://www.youtube.com/watch?v=qRPNuT080Hk

https://www.youtube.com/watch?v=uUupRagM7m0&list=PL2We04F3Y_41jYdadX55fdJplDvgNGENo

The GIT Repo for this tutorial can be found here: https://github.com/mmumshad/kubernetes-the-hard-way


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
#### kubectl rollout status deployment/my-deployment
#### kubectl rollout undo deployment/my-deployment
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
#### k get pods -L env -> to get labels of environment related pods
#### k get pods --selector env=dev -> to get pods from selector with the environment of dev.
#### kubectl label nodes node01 color=blue
#### kubectl taint nodes controlplane key=value:NoSchedule-
#### kubectl describe node controlplane
#### kubectl get daemonsets --all-namespaces -> to get daemonset which present in all namespace 
#### kubectl get ds <daemonset-name> -n <kube-system-namespacename> --> ds means daemonset, -n means namespace
#### kubectl get pods -A -> to findout static pods from all we use this command, but we get all pods will be listed here. So, at the end of pod if it mention with 'controlplane' name that we can considr as static pods.
#### kubectl run webapp-green --image=kodekloud/webapp-color --restart=Never --command -- webapp-color --color=green -> to create pod with command line argument in imperative way.
#### kubectl replace --force -f /tmp/<pod-name>  --> after tying to edit existing pod, but if u face issue then u can use replace command.


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
#### kubectl set image deployment/<deployment-name> <container-name>=kodekloud/webapp-color:v2

## Create a Service named redis-service of type ClusterIP to expose pod redis on port 6379

#### kubectl expose pod redis --port=6379 --name redis-service --dry-run=client -o yaml

#### kubectl create service nodeport nginx-svc --tcp=80:80 --node-port=30012

## Create a Service named nginx of type NodePort to expose pod nginx’s port 80 on port 30080 on the nodes:

#### kubectl expose pod nginx --type=NodePort --port=80 --name=nginx-service --dry-run=client -o yaml

#### press capital v and select the lines of yaml and click shift+. >so the alignment will be done

## Monitoring and Logging

#### git clone https://github.com/kodekloudhub/kubernetes-metrics-server.git
#### kubectl create -f kubernetes-metrics-server
#### k top node - to know which is having more utilization in nodes
#### k top pod - to know which is having more utilization in pods

## Configmap

#### k create configmap webapp-config-map --from-literal=<APP_COLOR=darkblue> --from-literal=<APP_OTHER=disregard>  --> to create configmap in imperative way
#### k run webapp-color --image=kodekloud/webapp-color --env="webapp-color=green" --labels="app=webapp-color" --> to create pod with environment values in imperative way.
