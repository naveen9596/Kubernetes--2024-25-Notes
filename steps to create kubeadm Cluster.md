sudo apt-get update
    3  curl -fsSL https://pkgs.k8s.io/core:/stable:/v1.29/deb/Release.key | sudo gpg --dearmor -o /etc/apt/keyrings/kubernetes-apt-keyring.gpg
    4  echo 'deb [signed-by=/etc/apt/keyrings/kubernetes-apt-keyring.gpg] https://pkgs.k8s.io/core:/stable:/v1.29/deb/ /' | sudo tee /etc/apt/sources.list.d/kubernetes.list
    5  sudo apt-get update
    6  sudo apt-get install -y kubelet kubeadm kubectl
    7  sudo apt-mark hold kubelet kubeadm kubectl
    8  sudo apt install docker.io
    9  sudo systemctl start docker
   10  sudo systemctl enable docker
   11  systemctl docker status
   12  docket --version
   13  sudo apt install docker.io
   14  docket --version
   15  systemctl docker status
   16  systemctl status docker
   17  sudo apt-get install curl
   18  sudo curl -s https://packages.cloud.google.com/apt/doc/apt-key.gpg | sudo apt-key add
   19  sudo apt-get update
   20  sudo swapoff -a
   21  free -h
   22  kubectl version --client
   23  sudo kubeadm init
