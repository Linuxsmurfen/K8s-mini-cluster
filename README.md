# Mini-k8s-cluster
A mini kubernetes cluster

## Overview
< Work in progress >   
A internal kuberenets cluster with three nodes. The cluster will be loadbalanced and use an ingress with wildcard DNS. The storage will be served by ceph and remote NFS storage.

### Hardware
![Hardware](/mini-k8s-cluster.jpg)

3 Elitedesk 800g2 nodes with
- 16GB Memory
- 256GB SSD
- 500GB NVMe

### Prereq
- [X] DNS domain wildcard
- [X] DHCP range

### Bootstrap
Setup the OS using PXE boot
- [ ] Baremetal provisioning

### K8s install
Configure the OS and install Kubernetes using Ansible
- [ ] Kubernetes installation using Kubeadm
- [ ] Network setup with Calico
- [ ] GitOps using Flux and SOPS

### Infra
Configure all base services using GitOps
- [ ] MetalLB
- [ ] Ingress-nginx
- [ ] NFS storage
- [ ] Rook-Ceph storage
- [ ] Velero

### Apps
Configure applications using GitOps
- [ ] HomeAssistant
- [ ] DeConz
- [ ] Gitea
- [ ] KubeView






