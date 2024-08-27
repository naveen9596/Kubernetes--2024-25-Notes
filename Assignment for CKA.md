Assignment: CKA Practice on Minikube
1. Cluster Setup and Configuration
Task: Set up a Minikube cluster with custom configurations.
Start Minikube with at least two CPUs and 4GB of memory.
Enable the metrics-server and dashboard addons.
Verify the status of the cluster and ensure that all components are running.
Access the Kubernetes dashboard.
2. Workloads and Scheduling
Task: Deploy and manage workloads.
Deploy an Nginx pod with a specific label (e.g., app=nginx).
Create a deployment for an application with at least three replicas.
Scale the deployment to five replicas.
Create a resource request and limit for CPU and memory in the deployment.
Implement a pod that uses node affinity to schedule it on a specific node.
Schedule a pod using a static manifest file directly on the control plane.
3. Networking
Task: Configure network policies and services.
Expose the Nginx deployment using a ClusterIP service.
Create a NetworkPolicy that restricts ingress to the Nginx pods to only allow traffic from a specific namespace.
Test the NetworkPolicy to ensure it's working as expected.
4. Storage
Task: Manage storage in the Minikube cluster.
Create a PersistentVolume (PV) and PersistentVolumeClaim (PVC) for the Nginx deployment.
Mount the PVC to the Nginx pod to serve static content.
Verify that the content is accessible via the Nginx service.
5. Logging and Monitoring
Task: Implement logging and monitoring.
Install and configure the kube-state-metrics addon.
Use kubectl logs to inspect the logs of a running pod.
Forward logs to a central logging system (e.g., Fluentd or ELK stack) if possible.
Set up an alert using Prometheus that triggers when the CPU usage of a pod exceeds 80%.
6. Cluster Maintenance
Task: Perform cluster maintenance tasks.
Create and restore a backup of etcd.
Upgrade the Minikube Kubernetes version.
Drain and cordon a node, then uncordon it.
Perform a rolling update of the deployment created earlier.
7. Troubleshooting
Task: Troubleshoot and resolve common issues.
Investigate and resolve a CrashLoopBackOff issue in a pod.
Debug a pod that is failing to start due to an image pull error.
Diagnose and fix an issue where a pod cannot communicate with a service in the same namespace.
