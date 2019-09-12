# A10-Ansible Demo ADC Project

Ansible + A10

This is an example ADC project to demonstrate the capabilities of [A10-Ansible](https://github.com/a10networks/a10-ansible).

The steps are mirrored from [A10's ADC Course](https://www.a10networks.com/support/training/adc-4-1/). 
Therefore it's best to follow the lab guide from the course when running this project.

## Dependencies (included as playbooks in this project)
 - installs correct ansible version
 - installs a10-ansible modules 

## An explanation of playbooks/a10_defaults.yml
A10-Ansible uses HTTP requests which requires, for authentication, the same 5 parameters in every one of its modules:
```yml
  a10_host: "{{ acos_host }}"
  a10_username: "{{ acos_username }}"
  a10_password: "{{ acos_password }}"
  a10_port: "{{ acos_port }}"
  a10_protocol: "{{ acos_protocol }}"
```
To save effort of including this in every module, which would also make your playbooks needlessly long, I've created this 
work-around in a10_defaults.yml. 

What a10_defaults.yml does is use Ansible builtin [module_defaults](https://docs.ansible.com/ansible/latest/user_guide/playbooks_module_defaults.html) to set default parameters for any modules.
I loop through the modules we'll be using in this project and append the five A10 parameters.
KEEP IN MIND - if you're using additional a10_modules, remember to add it to this list in a10_defaults.yml. 

## Lab 1: Load Balancing
 1. create slb server 
 2. create slb service groups
 3. create slb source nat pool
 4. create source ip persistence template
 5. create virtual server and vport
 
## Lab 2: HTTP Server
 1. create http layer 7 monitor
 2. create http nat pool
 3. create cookie persistence template
 4. create http templates
 5. create http VIP
 
## Lab 3: HTTPS Server
 1. manually create ssl keypair
 2. create ssl tempalte
 3. create ssl nat
 4. create https VIP
