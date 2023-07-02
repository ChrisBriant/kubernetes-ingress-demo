# Minikube Kubernetes Ingress Demo

Two apps, blue and green, deployed from simple pythonwebser app

Environment variables

APP_MESSAGE="This is the green app"
APP_BACKGROUND="#00FF00"

## Setup the ingress addon

minikube addons enable ingress
### Check
kubectl get pods -n ingress-nginx
### Get the controller class
kubectl describe deployment ingress-nginx-controller -n ingress-nginx

## Create all of the objects from the files

kubectl create -f <filename>
### Command below should display the port mappings and the ip Address
kubectl get ingress
### Run minikube ip and then modify the hosts file so that it maps like below
minikube ip
sudo vi /etc/hosts
<ip address from above command>  blue.example.com
<ip address from above command>  green.example.com


## Try example below which is the same as this demo

https://kubernetes.io/docs/tasks/access-application-cluster/ingress-minikube/


