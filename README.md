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
- [ ] GitOps using Flux

### Infra
Configure all base services
- [ ] Rook-Ceph storage
- [ ] NFS storage
- [ ] Ingress-nginx

### Apps
Configure applications
- [ ] HomeAssistant
- [ ] DeConz
- [ ] Gitea
