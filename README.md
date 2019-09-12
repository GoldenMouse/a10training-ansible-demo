# A10-Ansible Demo ADC Project

Ansible + A10

This is an example ADC project to demonstrate the capabilities of [A10-Ansible](https://github.com/a10networks/a10-ansible).

The steps are mirrored from [A10's ADC Course](https://www.a10networks.com/support/training/adc-4-1/). 
Therefore it's best to follow the lab guide from the course when running this project.

## Dependencies (included as playbooks in this project)
 - installs correct ansible version
 - installs a10-ansible modules 

## Lab 1: Load Balancing
 1. create slb server 
 2. create slb service groups
 3. create slb source nat pool
 4. create source ip persistence template
 5. create virtual server and vport
 
## Lab2: HTTP Server
 1. create http layer 7 monitor
 2. create http nat pool
 3. create cookie persistence template
 4. create http templates
 5. create http VIP
 
## Lab3: HTTPS Server
 1. manually create ssl keypair
 2. create ssl tempalte
 3. create ssl nat
 4. create https VIP
