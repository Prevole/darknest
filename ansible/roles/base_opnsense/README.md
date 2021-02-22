# Base - OPNSense

> A role to manage my OPNSense router

# Actions

## Reserve IP

Reserve an IP Address associated with a DNS record.

### Parameters

* `opnsense_action`: `reserve_ip`
* `opnsense_reserve_ip_mac_addr`: The MAC address of the device for which we reserve an IP
* `opnsense_reserve_ip_ip_addr`: The IP address we want to reserve
* `opnsense_reserve_ip_hostname`: The hostname associated to the device

### Example:

```yml
- name: Reserve host IP
  include_role:
    name: base_opnsense
  vars:
    opnsense_action: reserve_ip
    opnsense_reserve_ip_mac_addr: aa:bb:cc:dd:ee:ff
    opnsense_reserve_ip_ip_addr: 1.2.3.4
    opnsense_reserve_ip_hostname: sample
```
