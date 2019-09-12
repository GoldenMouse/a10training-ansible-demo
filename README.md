# A10-Ansible Demo ADC Project

Ansible + A10

This is an example ADC project to demonstrate the capabilities of [A10-Ansible](https://github.com/a10networks/a10-ansible).

The steps are mirrored from [A10's ADC Course](https://www.a10networks.com/support/training/adc-4-1/). 
Therefore it's best to follow the lab guide from the course when running this project.

## Dependencies (included as playbooks in this project)
 - installs correct ansible version
 - installs a10-ansible modules 

## Lab 1: Load Balancing
 - create slb server 
 - create slb service groups
 - create slb source nat pool
 - create source ip persistence template
 - create virtual server and vport
 
## Lab2: HTTP Server
 - create http layer 7 monitor
 - create http nat pool
 - create cookie persistence template
 - create http templates
 - create http VIP
 
## Lab3: HTTPS Server
 - manually create ssl keypair
 - create ssl tempalte
 - create ssl nat
 - create https VIP
