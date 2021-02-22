# Base - Inventory

> A role to manage the Ansible on the fly inventory

# Actions

## Add Host

Add a host to an inventory

### Parameters

* `inventory_action`: `add_host`
* `inventory_hostname [required]`: The hostname of the host to add to the inventory
* `inventory_name [required]`: A name for the inventory  
* `inventory_user [default: gl_host.user]`: User to connect to the host
* `inventory_password [default: gl_host.password]`: Password for the user to connect to the host
* `inventory_ssh_private_key_file [default: default(gl_host.private_key)] `: The SSH private key to connect to the host

### Example:

```yml
- name: Add host to inventory
  include_role:
    name: base_inventory
  vars:
    inventory_action: add_host
    inventory_name: inventory
    inventory_hostname: sample
    inventory_user: root
    inventory_password: 123456
    inventory_ssh_private_key_file: path/to/private/key
```
