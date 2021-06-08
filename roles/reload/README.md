# network.toolkit.reload

To use this multi-platform network automation reload role:

## Task example:

```
- name: use reload role
  include_role:
    name: reload
```

## Full Ansible Playbook example:

```
---
- name: reboot network devices
  hosts: routers
  gather_facts: no

  tasks:

    - name: use reload role
      include_role:
        name: reload
```
