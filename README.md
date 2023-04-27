# Managed-Kubernetes

An Ansible role that installs Kubernetes Cluster on Rhel and Ubuntu. More info about kubernetes: [link](https://kubernetes.io/)


## Requirements

Make sure, you made your vars file with valid path to custom template or you can use Default vars.

You need `ansible 2.13.7` to run this module.
The `ansible.posix.authorized_key` module [module](https://docs.ansible.com/ansible/latest/collections/ansible/posix/authorized_key_module.html#) is also necessary.


## Tasks descriptions

- main.yml - Run the OS check and run the relevant playbook
- setup-base-cni.yml - Setup CNI plugin
- setup-calico.yml - Setup Calico Pod Network
- setup-cilium.yml - Setup Cilium Pod Network
- setup-k8s-master.yml - Setup Cluster ControlPlane Node(s)
- setup-k8s-workers.yml - Setup Cluster Worker Node(s)
- setup-users.yml - Setup kube admin user
- rhel-install-k8s.yml- Install pkgs, containerd and kubernetes on Rhel / Rocky
- ubuntu-install-k8s.yml - Install pkgs, containerd and kubernetes on Ubuntu


## Example Playbook

Including an example of how to use your role (for instance, with variables passed in as parameters) is always nice for users too:
```
- hosts: servergroup
  become: true
  become_user: lee

  vars_files:
    - vars/main.yml
    
  roles:
    - nerve4-managed-kubernetes
```


## Maintainer Information
Lee | 2023
