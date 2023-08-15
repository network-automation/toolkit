# Requirements

Install Ansible Content Collection

```
ansible-galaxy collection install infra.controller_configuration
```

If you get stuck, check out their [Github repo documentation](https://github.com/redhat-cop/controller_configuration/tree/devel)

# Set environment variables 

For testing with CLI Ansible, you need to set some environment variables

- CONTROLLER_HOST
- CONTROLLER_USERNAME
- CONTROLLER_PASSWORD
- CONTROLLER_VERIFY_SSL

e.g. setup in your bashrc

```
export CONTROLLER_HOST='controller.mydomain'
export CONTROLLER_USERNAME='admin'
export CONTROLLER_PASSWORD='mypassword'
export CONTROLLER_VERIFY_SSL='false'
```