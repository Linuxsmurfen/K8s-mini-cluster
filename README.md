
# Overview
My playgroud for learning Kubernetes on baremetal.   
![Hardware](/mini-k8s-cluster.jpg)

[![Home-Internet](https://img.shields.io/uptimerobot/status/babb?color=important&label=home%20internet&style=flat-square&logo=opnSense&logoColor=white)](https://uptimerobot.com)
---

## Hardware
The hardware consists of three baremetal servers.

| Device             | Ram  | OS disk   | Data disk  |
|--------------------|------|-----------|------------|
|HP Elitedesk 800 G2 | 16GB | 256GB SSD | 500GB NVMe |
|HP Elitedesk 800 G2 | 16GB | 256GB SSD | 500GB NVMe |
|HP Elitedesk 800 G2 | 16GB | 256GB SSD | 500GB NVMe |



## Installation


| Hostname | OS              | Role         | IP            |
|----------|-----------------|--------------|---------------|
| k8s100   |Ubuntu 24.04 LTS | Controlplane | 192.168.1.170 |
| k8s101   |Ubuntu 24.04 LTS | Worker       | 192.168.1.171 |
| k8s102   |Ubuntu 24.04 LTS | Worker       | 192.168.1.172 |


### Settings
| Name                 | CIDR              |
|----------------------|-------------------|
| Node network         | 192.168.1.0/24    |
| Pod network          | 172.20.0.0/16     |
| Service network      | 10.96.0.0/12      |
| Loadbalancer network | 192.168.1.240-249 |


### Prereq
Make sure DHCP and DNS are configured
- [X] DNS domain wildcard
- [X] DHCP range

### Bootstrap
Install and configure the platform

- [X] OS provisioning using Netbootxyz
- [X] Ubuntu configuration using the autoinstall feature
- [X] Configure the OS using Ansible
- [X] Install kubernetes using kubeadm
- [ ] Network setup with Cilium
- [ ] GitOps using ArgoCD

### Infra
Configure all base services
- [X] MetalLB
- [X] Ingress-nginx
- [X] NFS storage
- [X] Rook-Ceph storage
- [X] Velero

### Apps
Configure applications
- [X] HomeAssistant
- [X] Gitea






