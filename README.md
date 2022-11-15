![Arista CVP Automation](https://img.shields.io/badge/Arista-CVP%20Automation-blue) ![Arista EOS Automation](https://img.shields.io/badge/Arista-EOS%20Automation-blue)

# AVD Arista Validated Design for Arista Test Drive (Level 3/CVP Lab Edition)

## About

This repository is configured to run [`arista.cvp`](https://github.com/aristanetworks/ansible-cvp) & [`arista.avd`](https://github.com/aristanetworks/ansible-avd) ansible collections against the Arista Test Drive (ATD) Topology (specifically the Level 3/CVP topology). 


## Lab Topology



## ATD Topology Device List

| Device | IP Address   |
| ------ | ------------ |
| spine1 |192.168.0.11 |
| spine2 |192.168.0.12 |
| spine3 |192.168.0.13 |
| leaf1  |192.168.0.21 |
| leaf2  |192.168.0.22 |
| leaf3  |192.168.0.23 |
| leaf4  |192.168.0.24 |

# Setup Your Environment

### Clone this Repository
Make sure you're in the persist directory, then clone this repository:

    git clone https://github.com/tonybourkesdnpros/AVD-Level3

### Install Components


    
# Reset Lab Environment to Default

### Add Lab Credentials

edit credentials in vscode: atd-inventory/inventory.yml 

(put your lab password in for ansible_password and ansible_ssh_pass)

### Run Playbook to Prepare CloudVision for AVD

The atd-reset-labs playbook will pull off any configlets that are not part of the base configuration (ATD-INFRA and switch-base configlets). It will also place the spines and leafs in the default containers, in case you've moved them for any reason. (Note: if you're using Studios, you need to de-provision all switches from Studios, as only Studios can remove Studios-generated configlets). 

    ansible-playbook playbooks/atd-reset-labs.yml
    
### Execute Tasks in CVP manually

The playbook will create tasks, but not a change control, so create a change control with the open tasks and execute the change control. 

# Build the Fabric

Run the fabric deploy playbook

    ansible-playbook playbooks/atd-fabric-deploy.yml 

This will take about 2-3 minutes, and will create a series of tasks in CloudVision. When the playbook is complete, create a change control from these tasks and execute it (you may see some errors, that's OK). 

Verify the fabric is configured
    show ip bgp summary
    show bgp evpn summary

## Run the other playbooks

# Run audit playbook to validate Fabric states
    ansible-playbook playbooks/atd-validate-states.yml

# Execute EOS_SNAPSHOT role to collect show commands
    ansible-playbook playbooks/atd-snapshot.yml


### License

Project is published under [Apache License]().
