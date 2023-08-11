# network.toolkit.user

To use this multi-platform network automation user role:

## Task example:

```
- name: load user role
  ansible.builtin.include_role:
    name: user
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
        name: user
```
