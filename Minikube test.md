minikube installation
create ec2 ubuntu with 2cpus and 2gb at least
#Update the system packages
sudo apt-get update -y
#Install Docker
sudo apt install docker.io -y
#Install minikube
-------------------------------------------
sudo wget https://storage.googleapis.com/miniku...
sudo cp minikube-linux-amd64 /usr/local/bin/minikube
--------------------------------------------
sudo chmod 755 /usr/local/bin/minikube
minikube version
#Install kubectl
curl -LO https://storage.googleapis.com/kubern...`curl -s https://storage.googleapis.com/kubern...`/bin/linux/amd64/kubectl
-----------------------------------------------
chmod +x ./kubectl
sudo mv ./kubectl /usr/local/bin/kubectl
kubectl version
#Start minikube
sudo usermod -aG docker $USER && newgrp docker
minikube start
minikube status
kubectl cluster-info
kubectl get nodes
