##  Kubernetes and Container Orchestration TOC

1. **What are Containers? (Comparison with VMs)**  
2. **Why do we need Container Orchestration?**  
3. **Introduction to Kubernetes and its Benefits**  
4. **Kubernetes Architecture (Master and Worker Nodes)**  

---

# **📌 Session Content: Introduction to Kubernetes and Container Orchestration**  

## **1️⃣ What are Containers? (Comparison with VMs)**  

### **Definition of Containers**  
- A **container** is a lightweight, portable, and self-sufficient unit that includes everything needed to run an application (code, runtime, system tools, and libraries).  
- Containers share the **same OS kernel** but run in isolated environments.  

### **Comparison: Containers vs Virtual Machines (VMs)**  

| Feature           | Virtual Machine (VM) | Container |
|------------------|---------------------|-----------|
| **OS** | Requires a full OS per VM | Shares the host OS kernel |
| **Size** | Large (GBs) | Lightweight (MBs) |
| **Startup Time** | Slow (minutes) | Fast (seconds) |
| **Isolation** | Strong, separate OS per VM | Process-level isolation |
| **Portability** | Less portable | Highly portable |

### **Benefits of Containers**  
✅ Faster startup and execution compared to VMs  
✅ Efficient resource utilization (no duplicate OS overhead)  
✅ Portability across different environments  
✅ Consistency between development, testing, and production  

---

## **2️⃣ Why do we need Container Orchestration?**  

### **Challenges with Running Containers in Production**  
While containers simplify application deployment, managing multiple containers across different machines introduces challenges such as:  
- **Scaling**: How to automatically adjust the number of containers?  
- **Load Balancing**: How to distribute traffic efficiently?  
- **Networking**: How do containers communicate across different hosts?  
- **Storage Management**: How to handle persistent data?  
- **Monitoring & Logging**: How to track performance and errors?  

### **What is Container Orchestration?**  
Container orchestration automates the deployment, scaling, networking, and management of containerized applications.  

### **Popular Container Orchestration Tools**  
- **Docker Swarm** – A simpler orchestration tool built into Docker  
- **Apache Mesos** – Used for large-scale container scheduling  
- **Kubernetes** – The most widely used, cloud-native orchestration tool  

🚀 **Kubernetes is the industry standard for container orchestration!**  

---

## **3️⃣ Introduction to Kubernetes and Its Benefits**  

### **What is Kubernetes?**  
- **Kubernetes (K8s)** is an open-source container orchestration platform designed to automate the deployment, scaling, and management of containerized applications.  
- Originally developed by **Google**, now maintained by the **Cloud Native Computing Foundation (CNCF)**.  

### **Key Features of Kubernetes**  
✅ **Automatic Scaling** – Increases or decreases the number of containers based on demand  
✅ **Load Balancing** – Efficiently distributes network traffic  
✅ **Self-healing** – Automatically restarts failed containers  
✅ **Service Discovery** – Provides internal DNS for communication between services  
✅ **Rolling Updates & Rollbacks** – Ensures zero-downtime deployments  
✅ **Persistent Storage** – Supports data persistence using volumes  

### **Why Use Kubernetes?**  
- **Standardization:** Works across cloud platforms (AWS, GCP, Azure, On-Premise)  
- **Efficiency:** Optimizes resource usage  
- **Fault Tolerance:** Ensures high availability  
- **DevOps Friendly:** Supports CI/CD workflows  

---

## **4️⃣ Kubernetes Architecture (Master and Worker Nodes)**  

### **High-Level Kubernetes Architecture**  

Kubernetes follows a **Master-Worker** architecture:  

### **⚡ Master Node (Control Plane)**
The **Master Node** manages the cluster and controls how applications are scheduled.  

🚀 **Key Components of the Master Node:**  
1. **API Server** – Central communication point for Kubernetes (handles `kubectl` commands)  
2. **Scheduler** – Assigns workloads (Pods) to worker nodes based on resource availability  
3. **Controller Manager** – Manages cluster state (e.g., scaling, pod health)  
4. **ETCD (Key-Value Store)** – Stores all cluster configurations and metadata  

---

### **⚡ Worker Nodes (Where Applications Run)**  
Worker Nodes execute workloads and communicate with the Master Node.  

🚀 **Key Components of a Worker Node:**  
1. **Kubelet** – Agent running on each node, ensuring containers are running as expected  
2. **Kube Proxy** – Manages networking and enables communication between Pods  
3. **Container Runtime** – Runs the containers (Docker, containerd, etc.)  

### **📌 Kubernetes Cluster Diagram**
```
+-------------------------------------------------------+
|                   Master Node                         |
|  +-----------------+  +-------------------------+    |
|  | API Server      |  | Scheduler               |    |
|  +-----------------+  +-------------------------+    |
|  | Controller Mgr  |  | ETCD (Key-Value Store)  |    |
|  +-----------------+  +-------------------------+    |
+-------------------------------------------------------+

                |       |       |

+-------------------------------------------------------+
|                  Worker Nodes                         |
|  +----------------+   +---------------------------+  |
|  | Kubelet       |   |  Kube Proxy                |  |
|  +----------------+   +---------------------------+  |
|  | Container Runtime |  | Containers (Pods)       |  |
|  +-------------------+  +-------------------------+  |
+-------------------------------------------------------+
```

---

## **🎯 Conclusion & Key Takeaways**  

✔ **Containers** are lightweight, fast, and portable, but need orchestration.  
✔ **Kubernetes** automates container deployment, scaling, and management.  
✔ **Master Node** controls the cluster; **Worker Nodes** run the workloads.  
✔ Kubernetes is **cloud-agnostic**, highly **scalable**, and supports **self-healing**.  

## hands-on activities

### **🛠️ Hands-on Activities for Kubernetes & Container Orchestration Session**  

These exercises will provide practical experience with Kubernetes concepts.

---

## **📌 Hands-on 1: Running a Container (Basic Docker & Kubernetes Setup)**  
### **Objective:** Understand how containers work before moving to Kubernetes  

### **Steps:**  
1️⃣ Install **Docker** and verify installation  
```sh
docker --version
```
2️⃣ Run an **Nginx container** locally  
```sh
docker run -d -p 8080:80 nginx
```
3️⃣ Check the running container  
```sh
docker ps
```
4️⃣ Stop and remove the container  
```sh
docker stop <container_id>
docker rm <container_id>
```
✅ **Outcome:** You have run a basic container and accessed it via a browser.

---

## **📌 Hands-on 2: Setting Up a Kubernetes Cluster (Minikube & kubectl)**  
### **Objective:** Set up Kubernetes on your local machine  

### **Steps:**  
1️⃣ Install **Minikube** (Skip if using Play with K8s/Katacoda)  
```sh
minikube start
```
2️⃣ Verify the cluster  
```sh
kubectl cluster-info
kubectl get nodes
```
✅ **Outcome:** You have a running Kubernetes cluster.

---

## **📌 Hands-on 3: Deploying Your First Pod in Kubernetes**  
### **Objective:** Deploy an application (Nginx) on Kubernetes  

### **Steps:**  
1️⃣ Create a **Pod** running Nginx  
```sh
kubectl run my-nginx --image=nginx --port=80
```
2️⃣ Verify the Pod is running  
```sh
kubectl get pods
```
3️⃣ Describe Pod details  
```sh
kubectl describe pod my-nginx
```
✅ **Outcome:** You have successfully deployed a containerized application in Kubernetes.

---

## **📌 Hands-on 4: Exposing a Pod with a Kubernetes Service**  
### **Objective:** Allow external access to the Nginx Pod  

### **Steps:**  
1️⃣ Expose the Pod using a **NodePort Service**  
```sh
kubectl expose pod my-nginx --type=NodePort --port=80
```
2️⃣ Find the service port  
```sh
kubectl get svc
```
3️⃣ Access the application in a web browser  
```sh
minikube service my-nginx --url
```
✅ **Outcome:** Your application is now accessible externally.

---

## **📌 Hands-on 5: Creating a Kubernetes Deployment**  
### **Objective:** Scale an application using Deployments  

### **Steps:**  
1️⃣ Create a **Deployment** for Nginx  
```sh
kubectl create deployment nginx-deploy --image=nginx
```
2️⃣ Scale the deployment to **3 replicas**  
```sh
kubectl scale deployment nginx-deploy --replicas=3
```
3️⃣ Check the number of running Pods  
```sh
kubectl get pods
```
✅ **Outcome:** Your app is now running with 3 replicas.

---

## **📌 Hands-on 6: Debugging and Logs in Kubernetes**  
### **Objective:** Check logs and troubleshoot issues  

### **Steps:**  
1️⃣ View logs of a Pod  
```sh
kubectl logs <pod-name>
```
2️⃣ SSH into a running container  
```sh
kubectl exec -it <pod-name> -- /bin/sh
```
✅ **Outcome:** You can now debug applications running in Kubernetes.

---

## **📌 Hands-on 7: Cleaning Up Kubernetes Resources**  
### **Objective:** Delete resources to free up space  

### **Steps:**  
1️⃣ Delete Deployment  
```sh
kubectl delete deployment nginx-deploy
```
2️⃣ Delete Service  
```sh
kubectl delete service my-nginx
```
3️⃣ Stop Minikube  
```sh
minikube stop
```
✅ **Outcome:** You have successfully cleaned up your cluster.

---

## **🎯 Summary of Hands-on Activities**  
🔹 **Run a container using Docker**  
🔹 **Deploy an application using Kubernetes**  
🔹 **Expose services to the external world**  
🔹 **Scale applications with Deployments**  
🔹 **Debugging and logs in Kubernetes**  

## custom scenarios Based Application:

### **🛠️ Custom Hands-on Scenarios for Your Kubernetes Training**  

To enhance your **4-hour Kubernetes session**, here are some **custom scenarios** tailored for your audience. These exercises cover real-world use cases and troubleshooting.

---

## **📌 Scenario 1: Deploy a Multi-Container Application (Nginx + Redis + Python App)**  
### **Objective:** Deploy a complete microservices-based app  

### **Steps:**  
1️⃣ **Create a Deployment for Nginx (Frontend)**  
```sh
kubectl create deployment frontend --image=nginx
kubectl expose deployment frontend --type=NodePort --port=80
```
2️⃣ **Create a Redis Pod (Backend Cache Service)**  
```sh
kubectl run redis --image=redis --port=6379
kubectl expose pod redis --type=ClusterIP --port=6379
```
3️⃣ **Deploy a Python Web App that connects to Redis**  
```sh
kubectl create deployment python-app --image=python:3.9
```
4️⃣ **Verify Inter-Service Communication**  
```sh
kubectl get svc
```
✅ **Outcome:** You have built a basic **microservices** architecture.

---

## **📌 Scenario 2: Kubernetes Rolling Updates & Rollbacks**  
### **Objective:** Deploy an application and perform a rolling update  

### **Steps:**  
1️⃣ **Deploy an old version of Nginx**  
```sh
kubectl create deployment nginx-update --image=nginx:1.19
```
2️⃣ **Update to a newer version (rolling update)**  
```sh
kubectl set image deployment/nginx-update nginx=nginx:1.21
```
3️⃣ **Check the rollout history**  
```sh
kubectl rollout history deployment/nginx-update
```
4️⃣ **Perform a rollback**  
```sh
kubectl rollout undo deployment/nginx-update
```
✅ **Outcome:** You understand **zero-downtime updates and rollbacks**.

---

## **📌 Scenario 3: Setting Resource Limits for Containers**  
### **Objective:** Configure CPU & Memory limits for a Kubernetes Pod  

### **Steps:**  
1️⃣ Create a YAML file (`resource-limit.yaml`)  
```yaml
apiVersion: v1
kind: Pod
metadata:
  name: limited-nginx
spec:
  containers:
  - name: nginx
    image: nginx
    resources:
      requests:
        memory: "64Mi"
        cpu: "250m"
      limits:
        memory: "128Mi"
        cpu: "500m"
```
2️⃣ Apply the YAML file  
```sh
kubectl apply -f resource-limit.yaml
```
3️⃣ Verify the resource limits  
```sh
kubectl describe pod limited-nginx
```
✅ **Outcome:** You learn **how to manage CPU & memory in Kubernetes**.

---

## **📌 Scenario 4: Using ConfigMaps and Secrets**  
### **Objective:** Store environment variables securely in Kubernetes  

### **Steps:**  
1️⃣ **Create a ConfigMap**  
```sh
kubectl create configmap app-config --from-literal=APP_ENV=production
```
2️⃣ **Create a Secret**  
```sh
kubectl create secret generic db-secret --from-literal=DB_PASSWORD=mysecurepassword
```
3️⃣ **Use them in a Deployment YAML**  
```yaml
apiVersion: v1
kind: Pod
metadata:
  name: configmap-secret-pod
spec:
  containers:
  - name: myapp
    image: myapp:latest
    env:
    - name: APP_ENV
      valueFrom:
        configMapKeyRef:
          name: app-config
          key: APP_ENV
    - name: DB_PASSWORD
      valueFrom:
        secretKeyRef:
          name: db-secret
          key: DB_PASSWORD
```
4️⃣ Apply the YAML file  
```sh
kubectl apply -f configmap-secret.yaml
```
✅ **Outcome:** You learn **how to securely store configurations**.

---

## **📌 Scenario 5: Deploying an Application with Auto-Scaling**  
### **Objective:** Automatically scale an application based on CPU usage  

### **Steps:**  
1️⃣ **Deploy an application**  
```sh
kubectl create deployment autoscale-nginx --image=nginx
kubectl expose deployment autoscale-nginx --type=LoadBalancer --port=80
```
2️⃣ **Enable Horizontal Pod Autoscaler (HPA)**  
```sh
kubectl autoscale deployment autoscale-nginx --cpu-percent=50 --min=1 --max=5
```
3️⃣ **Simulate CPU load to trigger auto-scaling**  
```sh
kubectl run load-generator --image=busybox -- /bin/sh -c "while true; do wget -q -O- http://autoscale-nginx; done"
```
4️⃣ **Check scaling**  
```sh
kubectl get hpa
kubectl get pods
```
✅ **Outcome:** You understand **how Kubernetes scales applications**.

---

## **📌 Scenario 6: Debugging a Failing Pod**  
### **Objective:** Learn Kubernetes troubleshooting techniques  

### **Steps:**  
1️⃣ **Deploy a faulty Pod**  
```sh
kubectl run badpod --image=nginx --command -- sleep 999999
```
2️⃣ **Check Pod logs**  
```sh
kubectl logs badpod
```
3️⃣ **Describe the Pod**  
```sh
kubectl describe pod badpod
```
4️⃣ **Exec into the Pod for debugging**  
```sh
kubectl exec -it badpod -- /bin/sh
```
✅ **Outcome:** You learn **real-world debugging skills**.

---

### **⏳ Suggested Time Breakdown for Hands-on Activities (4 Hours Total)**  

| Activity | Time (Minutes) |
|----------|--------------|
| **Hands-on 1: Running a Container** | 20 mins |
| **Hands-on 2: Kubernetes Setup** | 20 mins |
| **Hands-on 3: Deploying a Pod** | 30 mins |
| **Hands-on 4: Exposing a Service** | 30 mins |
| **Hands-on 5: Scaling an Application** | 30 mins |
| **Hands-on 6: ConfigMaps & Secrets** | 30 mins |
| **Hands-on 7: Rolling Updates & Rollbacks** | 20 mins |
| **Scenario 1: Multi-Container App** | 30 mins |
| **Scenario 2: Resource Limits** | 20 mins |
| **Scenario 3: Debugging Pods** | 30 mins |

✅ **Would you like any additional hands-on exercises?** 😊


### **🛠️ Additional Hands-on Exercises for Kubernetes Training**  

Here are some **advanced hands-on scenarios** to make your **4-hour Kubernetes training** more interactive and practical. These exercises cover security, networking, logging, monitoring, and advanced debugging.

---

## **📌 Scenario 7: Deploying a Stateful Application (MySQL in Kubernetes)**  
### **Objective:** Deploy a stateful application with persistent storage  
### **Steps:**  
1️⃣ **Create a Persistent Volume (PV) & Persistent Volume Claim (PVC)**  
```yaml
apiVersion: v1
kind: PersistentVolumeClaim
metadata:
  name: mysql-pvc
spec:
  accessModes:
    - ReadWriteOnce
  resources:
    requests:
      storage: 1Gi
```
```sh
kubectl apply -f mysql-pvc.yaml
```
2️⃣ **Deploy MySQL with PVC**  
```yaml
apiVersion: apps/v1
kind: Deployment
metadata:
  name: mysql
spec:
  replicas: 1
  selector:
    matchLabels:
      app: mysql
  template:
    metadata:
      labels:
        app: mysql
    spec:
      containers:
      - name: mysql
        image: mysql:5.7
        env:
        - name: MYSQL_ROOT_PASSWORD
          value: "password"
        volumeMounts:
        - name: mysql-storage
          mountPath: /var/lib/mysql
      volumes:
      - name: mysql-storage
        persistentVolumeClaim:
          claimName: mysql-pvc
```
```sh
kubectl apply -f mysql-deployment.yaml
kubectl get pods
```
✅ **Outcome:** You understand how to deploy **stateful applications with persistent storage**.

---

## **📌 Scenario 8: Network Policies in Kubernetes**  
### **Objective:** Restrict Pod-to-Pod communication using Network Policies  
### **Steps:**  
1️⃣ **Create a Network Policy to allow traffic only from a specific namespace**  
```yaml
apiVersion: networking.k8s.io/v1
kind: NetworkPolicy
metadata:
  name: allow-frontend
  namespace: default
spec:
  podSelector:
    matchLabels:
      app: backend
  ingress:
  - from:
    - podSelector:
        matchLabels:
          app: frontend
    ports:
    - protocol: TCP
      port: 80
```
```sh
kubectl apply -f network-policy.yaml
```
✅ **Outcome:** You have secured your Kubernetes cluster using **Network Policies**.

---

## **📌 Scenario 9: Monitoring Kubernetes with Prometheus and Grafana**  
### **Objective:** Set up **Prometheus & Grafana** for monitoring Kubernetes clusters  
### **Steps:**  
1️⃣ **Deploy Prometheus using Helm**  
```sh
helm repo add prometheus-community https://prometheus-community.github.io/helm-charts
helm install prometheus prometheus-community/kube-prometheus-stack
```
2️⃣ **Deploy Grafana**  
```sh
kubectl get svc -n monitoring | grep grafana
```
3️⃣ **Access Grafana UI** and visualize cluster metrics  
✅ **Outcome:** You have implemented **real-time monitoring** for Kubernetes.

---

## **📌 Scenario 10: Logging in Kubernetes with Fluentd + Elasticsearch + Kibana (EFK Stack)**  
### **Objective:** Centralized logging for Kubernetes logs  
### **Steps:**  
1️⃣ **Deploy Fluentd to collect logs**  
2️⃣ **Send logs to Elasticsearch**  
3️⃣ **Visualize logs in Kibana**  
✅ **Outcome:** You have built a **log aggregation system** for Kubernetes.

---

## **📌 Scenario 11: Running a Kubernetes Job (Batch Processing)**  
### **Objective:** Execute a **one-time batch job** in Kubernetes  
### **Steps:**  
1️⃣ **Create a Kubernetes Job**  
```yaml
apiVersion: batch/v1
kind: Job
metadata:
  name: batch-job
spec:
  template:
    spec:
      containers:
      - name: hello
        image: busybox
        command: ["echo", "Hello Kubernetes!"]
      restartPolicy: Never
```
2️⃣ **Run the job**  
```sh
kubectl apply -f job.yaml
kubectl get jobs
```
✅ **Outcome:** You have learned to **schedule and execute batch jobs** in Kubernetes.

---

## **📌 Scenario 12: Setting Up Kubernetes RBAC (Role-Based Access Control)**  
### **Objective:** Restrict user access in Kubernetes  
### **Steps:**  
1️⃣ **Create a Role & RoleBinding for read-only access to Pods**  
```yaml
apiVersion: rbac.authorization.k8s.io/v1
kind: Role
metadata:
  namespace: default
  name: pod-reader
rules:
- apiGroups: [""]
  resources: ["pods"]
  verbs: ["get", "watch", "list"]
```
```sh
kubectl apply -f role.yaml
```
2️⃣ **Create a ServiceAccount & Bind the Role**  
```yaml
apiVersion: rbac.authorization.k8s.io/v1
kind: RoleBinding
metadata:
  name: read-pods-binding
  namespace: default
subjects:
- kind: ServiceAccount
  name: read-only-user
  namespace: default
roleRef:
  kind: Role
  name: pod-reader
  apiGroup: rbac.authorization.k8s.io
```
```sh
kubectl apply -f rolebinding.yaml
```
✅ **Outcome:** You understand **user permissions in Kubernetes**.

---

### **⏳ Updated Time Breakdown for Hands-on Activities (4 Hours Total)**  

| Activity | Time (Minutes) |
|----------|--------------|
| **Basic Kubernetes Hands-on** | **(90 mins)** |
| Hands-on 1: Running a Container | 20 mins |
| Hands-on 2: Kubernetes Setup | 20 mins |
| Hands-on 3: Deploying a Pod | 30 mins |
| Hands-on 4: Exposing a Service | 20 mins |
| **Intermediate Kubernetes Hands-on** | **(90 mins)** |
| Hands-on 5: Scaling an Application | 30 mins |
| Hands-on 6: ConfigMaps & Secrets | 20 mins |
| Hands-on 7: Rolling Updates & Rollbacks | 20 mins |
| Scenario 1: Multi-Container App | 20 mins |
| **Advanced Kubernetes Hands-on** | **(60 mins)** |
| Scenario 7: Stateful Applications | 20 mins |
| Scenario 8: Network Policies | 20 mins |
| Scenario 9: Monitoring with Prometheus | 20 mins |
| **Security & Debugging** | **(40 mins)** |
| Scenario 10: Logging with EFK | 20 mins |
| Scenario 12: Kubernetes RBAC | 20 mins |

