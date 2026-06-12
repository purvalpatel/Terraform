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
