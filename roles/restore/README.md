# network.toolkit.restore

To use this multi-platform network automation restore role:

## Task example:

```
- name: load restore role
  include_role:
    name: restore
```

## Full Ansible Playbook example:

```
---
- name: restore router configurations
  hosts: routers
  gather_facts: no

  tasks:

    - name: load restore role
      include_role:
        name: restore
```
