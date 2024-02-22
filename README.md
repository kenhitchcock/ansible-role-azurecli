Ansible Role: Azure CLI
=========

Installs [Azure Command Line Interface](https://learn.microsoft.com/en-us/cli/azure/install-azure-cli-linux?pivots=dnf) on RHEL/CentOS or Debian/Ubuntu servers.

Requirements
------------

None.

Role Variables
--------------
Variables are preconfigured in the defaults/main.yml. Change only if the Microsoft Website updates.
```
azurecli_base_packages:
  - zip
  - unzip
  - azure-cli

azurecli_rpm_key: https://packages.microsoft.com/keys/microsoft.asc
azurecli_rhel8_repo_rpm: https://packages.microsoft.com/config/rhel/8/packages-microsoft-prod.rpm
azurecli_rhel9_repo_rpm: https://packages.microsoft.com/config/rhel/9.0/packages-microsoft-prod.rpm

```

Dependencies
------------

None.

Example Playbook
----------------

    - hosts: all
      roles:
         - { role: ansible-role-azurecli }

License
-------

MIT / BSD
