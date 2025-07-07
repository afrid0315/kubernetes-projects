# kubernetes-couponsLinkForExamination

https://couponcause.com/stores/linux-foundation/?matchtype=e&device=c&network=g&creative=643034165747&keyword=linux%20foundation%20promo&targetid=kwd-332562668813&position=&adgroup=49768141332&locaton=9061552&locationint=&campaign=879582855&extention=&gclick=Cj0KCQjwiYOxBhC5ARIsAIvdH50USOjmICLMWOjWucnqmyfhrrviZTjExV753MSejQwhj5CvWf7qGwMaAvBsEALw_wcB&gad_source=1&gclid=Cj0KCQjwiYOxBhC5ARIsAIvdH50USOjmICLMWOjWucnqmyfhrrviZTjExV753MSejQwhj5CvWf7qGwMaAvBsEALw_wcB


# Key Learning Materials:

https://notes.kodekloud.com/

https://collabnix.github.io/kubelabs/

https://www.twitch.tv/awstraininglive/videos - aws related

https://skillbuilder.aws/exam-prep/solutions-architect-associate?trk=e459a8a0-cbc6-4b8b-8504-6f86706fc9b5&sc_channel=em&mkt_tok=MTEyLVRaTS03NjYAAAGTSlHmZCoh9ESq9JdyPQwCkT7-njx_LpKbhMj6M5cokZzOUCW957XeWX9hqBMFmg-mpQXqekCdJwJ43X1eO-sD2DU5dhgRIpK-h2iqcRiXPcSf35SCpG69 - aws

https://kodekloud.com/courses/kubernetes-and-cloud-native-associate-kcna/ - Kubernetes and Cloud-Native Associate (KCNA) From KodeKloud

https://app.exampro.co/student/journey/kcna - Kubernetes and Cloud Native Associate (KCNA) From Exam pro or youtube platform which is free on both

https://training.linuxfoundation.org/training/introduction-to-kubernetes/

https://github.com/walidshaari/Kubernetes-and-Cloud-Native-Associate

https://github.com/moabukar/Kubernetes-and-Cloud-Native-Associate-KCNA/tree/main

https://kube.academy/

https://kubernetes.io/docs/home/

https://www.edx.org/learn/linux/the-linux-foundation-introduction-to-linux

https://www.edx.org/learn/cloud-computing/the-linux-foundation-introduction-to-cloud-infrastructure-technologies

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

## To apply a label color=blue to the node named node01

#### kubectl label node node01 color=blue

## To verify the label was applied

#### kubectl get nodes --show-labels

#### k get daemonsets --all-namespaces ---> to check daemonsets with all namespaces

## Configmap

#### k create configmap webapp-config-map --from-literal=<APP_COLOR=darkblue> --from-literal=<APP_OTHER=disregard>  --> to create configmap in imperative way
#### k run webapp-color --image=kodekloud/webapp-color --env="webapp-color=green" --labels="app=webapp-color" --> to create pod with environment values in imperative way.

## PriorityClasses

#### kubectl get pods -o custom-columns="NAME:.metadata.name,PRIORITY:.spec.priorityClassName" --> You can compare the priority classes on both pods using the above command

## to check service account

#### kubectl get serviceaccount -n kube-system

## to check cluster role binding

#### kubectl get clusterrolebinding

![image](https://github.com/afrid0315/kubernetes-projects/assets/126462435/2c068f7c-2c7c-4e12-a22e-129d088a712a)

![image](https://github.com/user-attachments/assets/a794913e-7d47-4d7c-8a41-ccb4f0294d7a)


25 Blogs to Learn 25 Kubernetes Concepts:

1) Kubernetes Architecture: https://t.co/PuZ6YEwSUV
2) POD Lifecycle: https://t.co/7yXNhSAEGN
3) etcd Setup: https://t.co/LmfuzAOoYc
4) etcd Locks: https://t.co/89EVkIkErU
5) crashloopbackoff: https://t.co/o5fXH5AGCf
6) OOMKilled: https://t.co/PodUWmEg8F
7) ImagePullBackOff: https://t.co/WcgKxGIFie
8) CreateContainerConfigError: https://t.co/gKOJEPOBqh
9) CreateContainerError: https://t.co/aYGv3rOxDP
10) RunContainerError: https://t.co/G5XYldSHOs
11) Node Disk Pressure: https://t.co/rE79HfTIq8
12) Node Not Ready:https://t.co/x93Bbczpqo
13) Pod Disruption Budget: https://t.co/iyuoQ6LyeK
14) RBAC: https://t.co/tPOuIhK9bn
15) DNS Optimization: https://t.co/6rnRM5yEnp
16) Kubernetes Controller: https://t.co/EcMvQ1JhSo
17) pod.yaml Breakdown: https://t.co/JhnPhMIDeK
18) Kubernetes Upgrades: https://t.co/43hVMt1JfU
19) KEDA vs Karpenter: https://t.co/NAaOZCkf7S
20) Operator vs Helm: https://t.co/eAsFl5DTAX
21) Kubernetes Air Gap: https://t.co/TB7ZEVWV7w
22) QoS Classes: https://t.co/pWOAiQSLDU 
23) Kubernetes CI/CD: https://t.co/0fo0r61rJD
24) Deployment Strategies: https://t.co/0iB7ZJjvf2
25) Security Contexts: https://t.co/kkforsRFOz
