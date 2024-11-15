# kublet-pods-creation

**step:1**
create ec2 instance
![Screenshot (8)](https://github.com/user-attachments/assets/11d2e23d-2013-4036-a5d1-f031ec76420e)

sudo su -

apt update -y

**step:2   install docker**
![Screenshot (6)](https://github.com/user-attachments/assets/ac4254fb-b1ca-452a-b327-30be7343d300)
sudo mv minikube-linux-amd64 /usr/local/bin/minikube

sudo chmod +x /usr/local/bin/minik be

sudo minikube version

sudo apt install curl wget apt-transport-https -y

sudo curl -LO "https://dl.k8s.io/release/$(curl -L -s https://dl.k8s.io/release/stable.txt)/bin/linux/amd64/kubectl"

sudo kubectl version --client

sudo curl -LO "https://dl.k8s.io/$(curl -L -s https://dl.k8s.io/release/stable.txt)/bin/linux/amd64/kubectl.sha256" sudo echo "$(cat kubectl.sha256) kubectl" | sha256sum --check sudo install -o root -g root -m 0755 kubectl /usr/local/bin/kubectl

sudo kubectl version --client

sudo kubectl version --client --output=yaml

sudo minikube start --driver=docker --force

creation of pod

kubectl run pod1 --image=nginx

kubectl get pods

vi Raviteja.yml

apiVersion: v1

kind: Pod

metadata:

name: nginx

spec:

containers:

name: nginx

image: nginx:1.14.2

ports:

containerPort: 80



