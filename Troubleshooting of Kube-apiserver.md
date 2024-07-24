 Typically happens when the API server is not running or is not accessible at the specified address and port.

The error "Unit kube-apiserver.service could not be found" suggests that the kube-apiserver service is not managed by systemd. This is typical for kubeadm deployments where the control plane components (including kube-apiserver) are managed as static pods by the kubelet.

Here’s how you can proceed to troubleshoot and ensure the kube-apiserver is running correctly:

1. **Check Static Pod Manifests:**
   The kube-apiserver should have a manifest file in `/etc/kubernetes/manifests/`. Check if the `kube-apiserver.yaml` file is present.

   ```bash
   ls /etc/kubernetes/manifests/
   ```

2. **Inspect the kube-apiserver Pod:**
   The kube-apiserver runs as a pod. Check the status of the pod:

   ```bash
   kubectl get pods -n kube-system
   ```

   Look for a pod named `kube-apiserver-<node-name>`. If it's not running, check its logs and describe it to see why it might be failing.

   ```bash
   kubectl logs kube-apiserver-<node-name> -n kube-system
   kubectl describe pod kube-apiserver-<node-name> -n kube-system
   ```

3. **Check Kubelet Logs:**
   Since the kubelet is responsible for managing the static pods, check the kubelet logs for any errors related to the kube-apiserver.

   ```bash
   sudo journalctl -u kubelet
   ```

4. **Verify Kubeconfig:**
   Ensure that your `kubectl` command is using the correct kubeconfig file. By default, it should be `/etc/kubernetes/admin.conf`.

   ```bash
   export KUBECONFIG=/etc/kubernetes/admin.conf
   ```

5. **Inspect Manifest Configuration:**
   Open the `kube-apiserver.yaml` file and verify that it is correctly configured. Check for correct values in fields like `advertise-address` and `secure-port`.

   ```bash
   cat /etc/kubernetes/manifests/kube-apiserver.yaml
   ```

6. **Restart Kubelet:**
   If you made any changes or just to ensure the kubelet picks up the correct configuration, restart the kubelet service.

   ```bash
   sudo systemctl restart kubelet
   ```

By following these steps, you should be able to identify the issue preventing the kube-apiserver from running correctly and ensure the control plane is operational.
