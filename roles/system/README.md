# network.toolkit.system

To use this multi-platform network automation system role:

## Task example:

```
- name: load system role
  include_role:
    name: system
```

## Full Ansible Playbook example:

```
---
- name: configure system properites
  hosts: routers
  gather_facts: no

  tasks:

    - name: load system role
      include_role:
        name: system
```
