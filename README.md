# Kubernetes Cluster Setup with Ansible & Terraform

This repository is designed to help you set up a Kubernetes cluster on 5 VMs using **Ansible** and **Terraform**. The setup includes 3 CentOS VMs and 2 Ubuntu VMs, all configured to run Kubernetes.

## Requirements

- 5 Linux VMs (CentOS 7/8 & Ubuntu 20.04/22.04)
- 2 GB RAM or more per machine
- 2 CPUs or more for control plane nodes
- Full network connectivity between all VMs
- Open Ports for Kubernetes communication (see Kubernetes documentation for port details)

## Project Structure

├── terraform/ │ ├── main.tf # Terraform configuration for creating VMs (if needed) │ ├── variables.tf # Variables for Terraform (VM configurations, etc.) │ └── outputs.tf # Outputs (VM details, IPs) ├── playbooks/ │ ├── kube_install.yml # Ansible playbook to install and configure Kubernetes │ ├── docker_install.yml # Ansible playbook to install Docker │ └── common_setup.yml # Ansible playbook for general setup (updates, prerequisites) ├── inventory/ │ └── hosts.ini # Inventory file for Ansible with VM details └── README.md # Project details and setup instructions

