revert-vsphere-vms

Ansible playbook to automate the proccess of vm's groups revert snapshot 

Edit /vars/main.yml in each role to add the follwoing details
For example

vcpass: "vcpass"
vcuser: "vcadmin"
vcenter: "vcenter-test" 
DC: "DC1"
snapshot: "snap-test"

Usage

ansible-playbook Revert-VMs.yaml

