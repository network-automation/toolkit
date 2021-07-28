# network.toolkit.banner

To use this multi-platform network automation banner role:

## Task example:

```
- name: load banner onto network device
  vars:
    - network_banner:  "{{ net_banner | default(None) }}"
    - banner_type: "{{ net_type | default('login') }}"
  include_role:
    name: network.toolkit.banner
```

## Full Ansible Playbook example:
```
---
- name: set router banners
  hosts: routers
  gather_facts: no

  tasks:
    - name: load banner onto network device
      vars:
        - network_banner:  "{{ net_banner | default(None) }}"
        - banner_type: "{{ net_type | default('login') }}"
      include_role:
        name: network.toolkit.banner
```

## Additional Info

There are two variables ready to use for extra_vars and/or Ansible Automation Platform [surveys](https://docs.ansible.com/ansible-tower/latest/html/userguide/job_templates.html#surveys).

The `network_banner` which is the text you want for the banner, and the `banner_type` which can be

- login
- motd
- exec (Cisco IOS only)
- incoming (Cisco IOS only)
- slip-ppp (Cisco IOS only)

This list of parameters is stored in each platform module:

- [Arista EOS](https://docs.ansible.com/ansible/latest/collections/arista/eos/eos_banner_module.html)
- [Cisco IOS](https://docs.ansible.com/ansible/latest/collections/cisco/ios/ios_banner_module.html)
- [Juniper Junos](https://docs.ansible.com/ansible/latest/collections/junipernetworks/junos/junos_banner_module.html)
