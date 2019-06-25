revert-vsphere-vms

Ansible playbook to automate the proccess of virtual machines revert snapshot 
The Role accepts a yaml with sublements as seen in the follwing example and reverts the virtual machine located under the vcenter listed in "vcenter:" in the vars file

---
config:
  - config_index: "0"
    env_hosts:
    - host_index: "0"
      ip: host1
      revert_vm: "true"
    - host_index: "1"
      ip: host2
      revert_vm: "false"


Edit revert-role-hosts/vars/main.yml to add the follwoing details
For example

vcpass: "vcpass"
vcuser: "vcadmin"
vcenter: "vcenter-test" 
DC: "DC1"
snapshot: "snap-test"

Usage

ansible-playbook Revert-VMs.yaml --extra-vars "env_yaml=/opt/hosts.yaml"



