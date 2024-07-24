Building a Kubernetes cluster using `kubeadm` on AWS with Ubuntu instances involves several steps. Here’s a detailed guide:

### Step-by-Step Installation Guide

#### 1. Launch Ubuntu Instances on AWS

- Launch the required number of Ubuntu instances (one master node and one or more worker nodes) from the AWS Management Console.
- Ensure that the security group associated with these instances allows necessary ports:
  - `6443` (Kubernetes API server)
  - `2379-2380` (etcd server client API)
  - `10250` (Kubelet API)
  - `10251` (kube-scheduler)
  - `10252` (kube-controller-manager)
  - `10255` (Read-only Kubelet API)
  - `30000-32767` (NodePort Services)

#### 2. Update and Upgrade the System
SSH into each instance and update the package list:
```bash
sudo apt-get update && sudo apt-get upgrade -y
```

#### 3. Disable Swap
Kubernetes requires swap to be disabled:
```bash
sudo swapoff -a
sudo sed -i '/ swap / s/^\(.*\)$/#\1/g' /etc/fstab
```

#### 4. Install Docker
Kubernetes uses Docker as the default container runtime. Install Docker CE:
```bash
sudo apt-get install -y apt-transport-https ca-certificates curl software-properties-common
curl -fsSL https://download.docker.com/linux/ubuntu/gpg | sudo apt-key add -
sudo add-apt-repository "deb [arch=amd64] https://download.docker.com/linux/ubuntu $(lsb_release -cs) stable"
sudo apt-get update
sudo apt-get install -y docker-ce
sudo systemctl start docker
sudo systemctl enable docker
```

#### 5. Add Kubernetes Repository
Add the Kubernetes APT repository:
```bash
sudo apt-get update && sudo apt-get install -y apt-transport-https curl
curl -s https://packages.cloud.google.com/apt/doc/apt-key.gpg | sudo apt-key add -
cat <<EOF | sudo tee /etc/apt/sources.list.d/kubernetes.list
deb https://apt.kubernetes.io/ kubernetes-xenial main
EOF
sudo apt-get update
```

#### 6. Install Kubernetes Packages
Install `kubeadm`, `kubelet`, and `kubectl`:
```bash
sudo apt-get install -y kubelet kubeadm kubectl
sudo apt-mark hold kubelet kubeadm kubectl
```

#### 7. Enable and Start kubelet
Enable and start the kubelet service:
```bash
sudo systemctl enable kubelet
sudo systemctl start kubelet
```

### Initializing the Cluster

#### 8. Initialize the Master Node
On the master node, initialize the cluster:
```bash
sudo kubeadm init --pod-network-cidr=10.244.0.0/16
```

Follow the instructions given by the `kubeadm init` command to set up your `kubectl` configuration:
```bash
mkdir -p $HOME/.kube
sudo cp -i /etc/kubernetes/admin.conf $HOME/.kube/config
sudo chown $(id -u):$(id -g) $HOME/.kube/config
```

#### 9. Install a Pod Network Add-on
To enable pod communication, install a pod network add-on. For example, to install Flannel:
```bash
kubectl apply -f https://raw.githubusercontent.com/coreos/flannel/master/Documentation/kube-flannel.yml
```

#### 10. Join Worker Nodes
On each worker node, use the `kubeadm join` command provided by the `kubeadm init` output on the master node. If you need to generate a new token or get the join command again, you can do so with:
```bash
sudo kubeadm token create --print-join-command
```

Run the provided `kubeadm join` command on each worker node to join them to the cluster.

### Verification

#### 11. Check Node Status
After joining the worker nodes, check the status of the nodes from the master:
```bash
kubectl get nodes
```

This command should list all nodes in the cluster with their statuses.

By following these steps, you should have a fully functional Kubernetes cluster using `kubeadm` on AWS Ubuntu instances.
