# HLAA - Home Lab Ansible Automation

> The purpose of this Ansible project is to automate the set up of the different parts of my Home Lab

## Service Definition

To define a service, we need to create a role following the naming convention `sv_<role_name>`.

Inside the service role directory, we create a file `definitions/main.yml` which contains the data to configure the host.

### All

* `def_host_amount [default: 1]`: The number of host of a specific type
* `def_host_name_pattern [required]`: The pattern to use in the host name
* `def_host_service [required]`: The name of the service (directly linked to the sv_<role_name>)
* `def_host_clusters [required]`: The clusters where the service is deployed 

### Playbook: configure_host_network

* `def_host_macaddr [required]`: The MAC address of the host (for DHCP reservation)
* `def_host_ipaddr [required]`:  The IP address of the host (for DHCP reservation)

## Execute a Playbook

To execute a playbook, most of the time, the command will be:

```bash
❯ ansible-playbook playbooks/<playbook_name>.yml -e @roles/sv_<service_name>/defintions/main.yml
```
