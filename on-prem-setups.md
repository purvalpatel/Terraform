Terraform is not limited to cloud providers like AWS, Azure, GCP.

#### Common on-prem terraform use-case:
- VMWare vShpere
- Proxmox VE
- Openstack
- Nutanix

### Modern Devops Flow:
```
Gitlab
  |
Terraform
  |
Create Infrastructure  -> Create VM, Network, Storage
  |
  |
Ansible
  |
configure Infrastructure  -> Install packages
  |
  |
ArgoCD -> Prometheus, Grafana, Jupyterhub, MLFlow, vLLM
  |
Deploy Applications 
```

## Setup Steps:

### 1. Create user and token in proxmox.
- Proxmox -> Datacenter -> Permissions -> user
- Add user : `terraform@pve`
- API TOken : `terraform-token`
- Permissions : Select users and add two tokens : `PVEAuditor, PVEAudit`

### 2. Create VM Template:
- Install Ubuntu 24.04 Server OS
- cloud init enabled : `apt install cloud-init`
- QEMU guest agent enabled : `apt-get install qemu-guest-agent`

