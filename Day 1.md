## Kubernetes

## 1.Overview

- Kubernetes is a portable, extensible, open source platform for managing containerized workloads and services, that facilitates both declarative configuration and automation. It has a large, rapidly growing ecosystem. Kubernetes services, support, and tools are widely available.

- K8s as an abbreviation results from counting the eight letters between the "K" and the "s". Google open-sourced the Kubernetes project in 2014. Kubernetes combines over 15 years of Google's experience running production workloads at scale with best-of-breed ideas and practices from the community.

![image](https://github.com/naveen9596/Kubernetes--IAS-Batch/assets/108785228/12065ed2-021e-4545-afc8-2d96ec2ec4ae)

**Traditional deployment era:** Early on, organizations ran applications on physical servers. There was no way to define resource boundaries for applications in a physical server, and this caused resource allocation issues.

**Virtualized deployment era:**  As a solution, virtualization was introduced. It allows you to run multiple Virtual Machines (VMs) on a single physical server's CPU. Virtualization allows applications to be isolated between VMs and provides a level of security as the information of one application cannot be freely accessed by another application.

**Container deployment era:** Containers are similar to VMs, but they have relaxed isolation properties to share the Operating System (OS) among the applications. Therefore, containers are considered lightweight. Similar to a VM, a container has its own filesystem, share of CPU, memory, process space, and more. As they are decoupled from the underlying infrastructure, they are portable across clouds and OS distributions.

## 2.Why you need Kubernetes and what it can do
Containers are a good way to bundle and run your applications. In a production environment, you need to manage the containers that run the applications and ensure that there is no downtime. For example, if a container goes down, another container needs to start. Wouldn't it be easier if this behavior was handled by a system?

That's how Kubernetes comes to the rescue! Kubernetes provides you with a framework to run distributed systems resiliently. It takes care of scaling and failover for your application, provides deployment patterns, and more. **For example:** Kubernetes can easily manage a canary deployment for your system.

## 3.Kubernetes provides you with:

**A.Service discovery and load balancing** 
Kubernetes can expose a container using the DNS name or using their own IP address. If traffic to a container is high, Kubernetes is able to load balance and distribute the network traffic so that the deployment is stable.
**B.Storage orchestration** 
Kubernetes allows you to automatically mount a storage system of your choice, such as local storages, public cloud providers, and more.
**Automated rollouts and rollbacks** You can describe the desired state for your deployed containers using Kubernetes, and it can change the actual state to the desired state at a controlled rate. For example, you can automate Kubernetes to create new containers for your deployment, remove existing containers and adopt all their resources to the new container.
**Automatic bin packing** You provide Kubernetes with a cluster of nodes that it can use to run containerized tasks. You tell Kubernetes how much CPU and memory (RAM) each container needs. Kubernetes can fit containers onto your nodes to make the best use of your resources.
**Self-healing** Kubernetes restarts containers that fail, replaces containers, kills containers that don't respond to your user-defined health check, and doesn't advertise them to clients until they are ready to serve.
**Secret and configuration management** Kubernetes lets you store and manage sensitive information, such as passwords, OAuth tokens, and SSH keys. You can deploy and update secrets and application configuration without rebuilding your container images, and without exposing secrets in your stack configuration.
**Batch execution** In addition to services, Kubernetes can manage your batch and CI workloads, replacing containers that fail, if desired.
**Horizontal scaling** Scale your application up and down with a simple command, with a UI, or automatically based on CPU usage.
**IPv4/IPv6 dual-stack** Allocation of IPv4 and IPv6 addresses to Pods and Services
**Designed for extensibility** Add features to your Kubernetes cluster without changing upstream source code.






** DevOps Prerequisite course**
===========================
```
linux basics
virtual box networking
vagrant
networking basics
programming basics
database basics
git
apache web server
ips and ports
ssl & tls basics
yaml
```


Linux for Beginners

linux shell
kernel
runlevels
filetypes
rpm
yum
dpkg
apg
vi editor
networking
dns
ssh
scp
iptables
systemd
nfs
lvm

## Docker
``containers
images
volumes
container
orchestration
networking
``





