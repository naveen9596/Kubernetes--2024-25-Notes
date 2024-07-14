   
Kubernetes AWS-Ubuntu22.04 Machine Commands:
=============================================

```
	sudo -i
	hostnamectl set-hostname master
	bash

    1  sudo apt-get update
    2  sudo apt-get install -y apt-transport-https ca-certificates curl gpg
    3  curl -fsSL https://pkgs.k8s.io/core:/stable:/v1.29/deb/Release.key | sudo gpg --dearmor -o /etc/apt/keyrings/kubernetes-apt-keyring.gpg
    4  echo 'deb [signed-by=/etc/apt/keyrings/kubernetes-apt-keyring.gpg] https://pkgs.k8s.io/core:/stable:/v1.29/deb/ /' | sudo tee /etc/apt/sources.list.d/kubernetes.list
    5  sudo apt-get update
    6  sudo apt-get install -y kubelet kubeadm kubectl
    7  sudo apt-mark hold kubelet kubeadm kubectl
    8  sudo apt-get install -y kubelet kubeadm kubectl (Optional)
    9  yum install docker
   10  clear
   11  sudo apt install docker.io
   12  sudo systemctl start docker
   13  sudo systemctl enable docker
   15  docker --version
   16  clear
   17  sudo apt-get install curl
   18  sudo curl -s https://packages.cloud.google.com/apt/doc/apt-key.gpg | sudo apt-key add
   19  sudo apt-get update
   20  sudo swapoff -a
	#The command sudo swapoff -a is used to disable all swap space on a Linux system. Swap space is used to extend the amount of available memory by 	using disk space. Disabling it can be useful for certain performance tuning tasks or when you're planning to resize or remove swap partitions.

   21. 	free -h				# Verifying the Change** 
					# To verify that the swap space has been successfully disabled, you can use the following command


   21. kubectl version --client 	# To Check the version of kubectl
```
```
   22  sudo kubeadm init

	# Then you can join any number of worker nodes by running the following on each as root:
	kubeadm join 172.30.3.115:6443 --token kyc11y.58oskoe7hpj06zv4 \
        --discovery-token-ca-cert-hash sha256:3d49b9d654c851d522812decb624e004e0ed169d735ea692619fa7e3e72b59de
```

   23  history
