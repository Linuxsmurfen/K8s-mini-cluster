# Mini-k8s-cluster
A mini kubernetes cluster

## Overview

### Hardware
![Hardware](/mini-k8s-cluster.jpg)

3 Elitedesk 800g2 nodes with
- 16GB Memory
- 256GB SSD
- 500GB NVMe


### Bootstrap
Set everything up using PXE and Ansible
- [ ] Baremetal provisioning using PXE boot
- [ ] Kubernetes installation using Ansible
- [ ] GitOps using Flux and SOPS

### Infra
Configure all base services using GitOps
- [ ] Rook-Ceph storage
- [ ] NFS storage
- [ ] Ingress-nginx
- [ ] Velero

### Apps
Configure applications using GitOps
- [ ] HomeAssistant
- [ ] DeConz
- [ ] Gitea
- [ ] KubeView






