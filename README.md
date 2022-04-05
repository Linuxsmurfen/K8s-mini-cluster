# Overview
My playgroud for learning Kubernetes on baremetal.


### Hardware
![Hardware](/mini-k8s-cluster.jpg)

Three HP Elitedesk 800g2 nodes with
- 16GB Memory
- 256GB SSD
- 500GB NVMe

### Prereq
Make sure DHCP and DNS are configured
- [X] DNS domain wildcard
- [X] DHCP range

### Bootstrap
Install and prepare the OS
- [X] Autoinstall
- [ ] (Baremetal provisioning)
- [ ] Prepare the OS

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






