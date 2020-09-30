# AnsibleFest  - 2020 Check Point demo use cases

## Overview

This repository contains the Ansible roles and playbooks used to demonstrate the following use cases at AnsibleFest 2020
1. UseCaseA.yml - DevOps pets vs cattle concept for the service model
2. UsecaseB.yml - Security Orchestration, Automation and Response (SOAR)
3. UsecaseC.yml - DevSecOps model to accelerate application deployment
4. UsecaseD.yml - Automate repetitive and time-consuming maintenance tasks

## What does it do?

The Ansible playbooks leverage the Check Point modules for Ansible to embrace the DevSecOps mindset to accelerate secure application deployment and automate various tasks for the identification, search, and response to security events

The Ansible playbooks will also consume the same modules in automated workflows to support the deployment and maintenance of both physical and virtualized next-generation firewalls

## Requirements

- [Ansible](https://docs.ansible.com/ansible/latest/installation_guide/intro_installation.html) - Version 2.9 or later
- [Ansible check_point.mgmt collection](https://galaxy.ansible.com/check_point/mgmt) - Included by default from version Ansible 2.9
  - **Note:** It is recommended to download the latest version from galaxy
- [Check Point Security Management and Gateway](https://supportcenter.checkpoint.com/supportcenter/portal?eventSubmit_doGoviewsolutiondetails=&solutionid=sk160736) - Version R80.40 or later

## Usage

1. Clone the repository
2. Create a set_env_var.sh file with content like this (use your details):

```
export VAR_mgmt_api_user="Check Point Admin User"
export VAR_mgmt_api_password="Check Point Admin User"
export VAR_mgmt_api_key="Check Point Admin API Key"      
export VAR_mgmt_hostname="Check Secuity Management Hostname"
export VAR_mgmt_IP="Check Secuity Management IP"

``` 
3. From a command line, export your mgmt variables
> ```
> source ./set_env_var.sh
>```

4. From a command line, execute the playbooks
> ```
> ansible-playbook UseCaseA.yml
> ansible-playbook UseCaseB.yml
> ansible-playbook UseCaseC.yml
> ansible-playbook UseCaseD.yml
> ```


## References
* [sk114661 - Automate your management server using "Ansible"](https://supportcenter.checkpoint.com/supportcenter/portal?eventSubmit_doGoviewsolutiondetails=&solutionid=sk114661?tocpath=Posture%20Management%7CThe%20CloudGuard%20Dome9%20GSL%20Language%7C_____0)
* [Check Point Ansible collections](https://galaxy.ansible.com/check_point)
* [Check Point Ansible modules documentation](https://docs.ansible.com/ansible/2.9/modules/list_of_network_modules.html#check-point)
