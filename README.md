Ansible role for sudoers-d
==================================

Add entries to sudoers drop in directory

[![GitHub Actions](https://github.com/mongodb-ansible-roles/ansible-role-sudoers-d/workflows/Molecule%20Test/badge.svg)](https://github.com/mongodb-ansible-roles/ansible-role-sudoers-d/actions?query=workflow%3A%22Molecule+Test%22)
[![GitHub Actions](https://github.com/mongodb-ansible-roles/ansible-role-sudoers-d/workflows/Release/badge.svg)](https://github.com/mongodb-ansible-roles/ansible-role-sudoers-d/actions?query=workflow%3A%22Release%22)

Requirements
------------

None

Role Variables
--------------

| Name | Description | Type | Default | Required |
|------|-------------|:----:|:-------:|:--------:|
| `sudoers_commands` | Array of files to add to /etc/sudoers.d/ directory | array | "" | yes |

Dependencies
------------

None

Example Playbook
----------------

```yaml
- hosts: all
  roles:
    - role: ansible-role-sudoers-d
      vars:
        sudoers_commands:
          - user: test_user
            commands: /usr/bin/pwd
            dest: /etc/sudoers.d/pwd
```

License
-------

[Apache License](LICENSE)
