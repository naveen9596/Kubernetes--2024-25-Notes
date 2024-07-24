``` 1  sudo apt-get update
    2  sudo apt-get install -y apt-transport-https ca-certificates curl gpg
    3  curl -fsSL https://pkgs.k8s.io/core:/stable:/v1.29/deb/Release.key | sudo gpg --dearmor -o /etc/apt/keyrings/kubernetes-apt-keyring.gpg
    4  echo 'deb [signed-by=/etc/apt/keyrings/kubernetes-apt-keyring.gpg] https://pkgs.k8s.io/core:/stable:/v1.29/deb/ /' | sudo tee /etc/apt/sources.list.d/kubernetes.list
    
    5  sudo apt-get update
    6  sudo apt-get install -y kubelet kubeadm kubectl
    7  sudo apt-mark hold kubelet kubeadm kubectl
    8  sudo apt install docker.io
    9  sudo systemctl start docker
   10  sudo systemctl enable docker
   11  sudo systemctl status docker
   12  sudo apt-get install curl
   13  sudo curl -s https://packages.cloud.google.com/apt/doc/apt-key.gpg | sudo apt-key add
   14  sudo apt-get update
   15  sudo swapoff -a
   16  free -h
   17  kubectl version --client
   18  sudo kubeadm init
   19  kubeadm join 172.30.3.56:6443 --token 3bw6mw.muag8bxc5cnxaqnh         --discovery-token-ca-cert-hash sha256:d9abfa8e1ac046914c84f4ba7fcbec86d0985c8a5a7d53a00c38ab07395e0f6c 
   20  kubectl version --client
   21  sudo apt-get update
   22  kubeadm join 172.30.3.56:6443 --token 3bw6mw.muag8bxc5cnxaqnh         --discovery-token-ca-cert-hash sha256:d9abfa8e1ac046914c84f4ba7fcbec86d0985c8a5a7d53a00c38ab07395e0f6c 
   23  clear
   24  sudo kubeadm reset -f
   25  sudo rm -rf /etc/kubernetes
   26  sudo rm -rf /var/lib/etcd
   27  sudo rm -rf ~/.kube
   28  sudo lsof -i :10250
   29  sudo systemctl stop kubelet
   30  sudo systemctl disable kubelet
   31  clear
   32  kubeadm join 172.30.3.56:6443 --token 3bw6mw.muag8bxc5cnxaqnh         --discovery-token-ca-cert-hash sha256:d9abfa8e1ac046914c84f4ba7fcbec86d0985c8a5a7d53a00c38ab07395e0f6c 
   33  systemctl enable kubelet
   34  systemctl start kubelet
   35  systemctl status kubelet
   36  kubectl config view
   37  export KUBECONFIG=/etc/kubernetes/admin.conf
   38  kubectl config view
   39  kubectl apply -f https://docs.projectcalico.org/manifests/calico.yaml
   40  clear
   41  history
```
