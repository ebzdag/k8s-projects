# kubernetes

sudo apt install bind9-host
host -t NS k8s.ebozdag.online

kubectl attach helloworld -i
kubectl logs helloworld
kubectl exec -it helloworld -- bash

kubectl run -i --tty busybox --image=busybox --restart=Never -- sh

kubectl create deployment hello-minikube --image=k8s.gcr.io/echoserver:1.4
kubectl expose deployment hello-minikube --type=NodePort --port=8080

kops create cluster --name=k8s.ebozdag.online --state=s3://kops-state-work --zones=us-west-2a --node-count=2 --node-size=t2.micro --master-size=t2.micro --dns-zone=k8s.ebozdag.online

