```
root@master:/# history
    1  sudo apt-get update
    2  curl -fsSL https://pkgs.k8s.io/core:/stable:/v1.29/deb/Release.key | sudo gpg --dearmor -o /etc/apt/keyrings/kubernetes-apt-keyring.gpg
    3  echo 'deb [signed-by=/etc/apt/keyrings/kubernetes-apt-keyring.gpg] https://pkgs.k8s.io/core:/stable:/v1.29/deb/ /' | sudo tee /etc/apt/sources.list.d/kubernetes.list
    4  sudo apt-get update
    5  sudo apt-get install -y kubelet kubeadm kubectl
    6  sudo apt-mark hold kubelet kubeadm kubectl
    7  sudo apt install docker.io
    8  sudo systemctl start docker
    9  sudo systemctl enable docker
   10  docker --version
   11  sudo apt-get install curl
   12  sudo curl -s https://packages.cloud.google.com/apt/doc/apt-key.gpg | sudo apt-key add
   13  sudo apt-get update
   14  sudo swapoff -a
   15  free -h
   16  kubectl version --client
   17  sudo kubeadm init
   18  kubectl get nodes
   19  clear
   20  sudo systemctl status kube-apiserver
   21  sudo systemctl start kube-apiserver
   22  export KUBECONFIG=/etc/kubernetes/admin.conf
   23  sudo journalctl -u kube-apiserver
   24  cd /etc/kubernetes/manifests
   25  ls -la
   26  cd kube-apiserver.yaml
   27  vi kube-apiserver.yaml
   28  sudo systemctl restart kubelet
   29  cd ..
   30  cd 
   31  cd ..
   32  sudo systemctl status kube-apiserver
   33  kubectl get pods -n kube-system
   34  kubectl logs kube-apiserver-kube-apiserver-master -n kube-system
   35  kubectl describe pod kube-apiserver-master -n kube-system
   36  kubectl logs kube-apiserver-master -n kube-system
   37  sudo journalctl -u kubelet
   38  ls
   39  cd /etc/kubernetes/manifests
   40  ls
   41  cat kube-apiserver.yaml
   42  apt install net-tools
   43  clear
   44  hostnamectl set-hostname master
   45  bash
   46  netstat -tnpl
   47  clear
   48  kubectl get nodes
   49  clear
   50  cd /etc/kubernetes/manifests
   51  ls
   52  cd
   53  cd .kube/
   54  ls
   55  kubectl config view
   56  cd etcd
   57  cd /etcd
   58  cd /etc/systemd/
   59* [A
   60  cd ..
   61  ls
   62  cd ..
   63  kubectl get nodes
   64  kubectl get nodes --kubeconfig /etc/kubernetes/kubelet.conf
   65* 
   66* 
   67  kubectl describe node master
   68  kubectl describe node master --kubeconfig /etc/kubernetes/kubelet.conf
   69  ls
   70  kubectl get nodes --kubeconfig /etc/kubernetes/kubelet.conf
   71  kubectl describe node master --kubeconfig /etc/kubernetes/kubelet.conf
   72  systemctl status docker
   73  kubectl describe node master --kubeconfig /etc/kubernetes/kubelet.conf
   74  kubectl apply -f https://docs.projectcalico.org/manifests/calico.yaml
   75  kubectl apply -f https://docs.projectcalico.org/manifests/calico.yaml --validate=false
   76  kubectl apply -f https://docs.projectcalico.org/manifests/calico.yaml --validate=false --kubeconfig /etc/kubernetes/kubelet.conf
   77  clear
   78  curl https://raw.githubusercontent.com/projectcalico/calico/v3.28.0/manifests/calico.yaml -O
   79  kubectl apply -f calico.yaml --kubeconfig /etc/kubernetes/kubelet.conf
   80  export KUBECONFIG=/etc/kubernetes/admin.conf
   81  kubectl apply -f https://docs.projectcalico.org/manifests/calico.yaml
   82  cd .kube
   83  kubectl config view
   84  kubectl get nodes
   85  history
```
