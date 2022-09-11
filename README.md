paulrentschler.redis
====================

[![MIT licensed][mit-badge]][mit-link]

Installs and configures the Redis daemon on Ubuntu or RedHat Linux machines.

Requirements
------------

On RedHat-based distributions, requires the EPEL repository (use the `paulrentschler.repo-epel` role to ensure EPEL is available).


Role Variables
--------------

The following variables are available with defaults defined in `defaults/main.yml`:


### TODO: more information here




Dependencies
------------

None.


Example Playbook
----------------

Simple version:

```yaml
---
- hosts: all
  roles:
    - paulrentschler.redis
```


Have double the number of databases, require a password, and do not save the DB to disk:

```yaml
---
- hosts: all
  roles:
     - role: paulrentschler.redis
       vars:
         redis_databases: 32
         redis_requirepass: "{{ vaulted_redis_password }}"
         redis_save: []
```


License
-------

[MIT][mit-link]


Author Information
------------------

Created by Paul Rentschler in 2022.

Based heavily on the [geerlingguy.redis](https://galaxy.ansible.com/geerlingguy/redis) role created by [Jeff Geerling](https://www.jeffgeerling.com/).


[mit-badge]: https://img.shields.io/badge/license-MIT-blue.svg
[mit-link]: https://github.com/paulrentschler/ansible-role-redis/blob/main/LICENSE
