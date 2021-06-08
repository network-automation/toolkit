# network.toolkit.backup

To use this multi-platform network automation backup role:

```
- name: retrieve router configurations
  hosts: all
  gather_facts: no

  tasks:
    - name: backup configuration
      include_role:
        name: network.toolkit.backup
      when: ansible_network_os is defined
```

Backups are currently stored on the ansible-1 control node as part of the [network workshop](https://ansible.github.io/workshops/exercises/ansible_network/).  For a full example please refer to the [network_backup.yml](../../network_backup.yml) example.
