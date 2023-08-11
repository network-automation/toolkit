# network.toolkit.vlans

To use this multi-platform network automation vlans role:

## Task example:

```
- name: load user role
  ansible.builtin.include_role:
    name: network.toolkit.vlans
```

## Full Ansible Playbook example:

```
---
- name: configure user on network devices
  hosts: routers
  gather_facts: no

  tasks:
    - name: load user role
      ansible.builtin.include_role:
        name: network.toolkit.vlans
```
