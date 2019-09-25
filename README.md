# minikube

## Install on MacOS

curl -LO https://storage.googleapis.com/kubernetes-release/release/$(curl -s https://storage.googleapis.com/kubernetes-release/release/stable.txt)/bin/darwin/amd64/kubectl && chmod +x kubectl && sudo mv kubectl /usr/local/bin

curl -Lo minikube https://storage.googleapis.com/minikube/releases/latest/minikube-darwin-amd64 && chmod +x minikube && sudo mv minikube /usr/local/bin/

minikube start

## Run & expose container

kubectl run my-app --image=u1ih/hello --port=8080

kubectl expose deployment my-app --type=NodePort --port=8080 --target-port=8080

minikube service my-app --url
