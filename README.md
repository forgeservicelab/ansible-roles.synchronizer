Synchronizer
============

Sets up the environment to recurringly run the sync script to pull data from Insightly into LDAP.

Role Variables
--------------

### Defaults:
  - `ldap_host` - FQDN or IP of the LDAP server to update (defaults to `localhost`).
  - `ldap_bind_cn` - CN of the account used to bind and update LDAP, it must have write rights (defaults to `admin`).

### Variable Parameters and/or global scope variables:
  - `ìnsightly_api_key` - Insightly API key.
  - `ldap_admin_passsword` - LDAP password of the bind account above.
  - `os_admin_user` - Administrator username for OpenStack.
  - `os_admin_pwd` - Administrator password for OpenStack.
  - `os_admin_tenant` - Tenant for the OpenStack administrator account.
  - `redmine_api_key` - REST API key for Redmine.

Example Playbook
----------------

```YAML
    - hosts: servers
      roles:
         - role: synchronizer
           ldap_host: my.ldap-host.com
           ldap_bind_cn: Manager
```

License
-------

GPLv3

Author Information
------------------

Jorge Rodriguez (A.K.A. Tiriel) <jorge.rodriguez@forgeservicelab.fi>
FORGE ServiceLab.
