# Ansible Role: Autoupdate

[![Build Status](https://travis-ci.org/tschifftner/ansible-role-autoupdate.svg?branch=master)](https://travis-ci.org/tschifftner/ansible-role-autoupdate)

Installs autoupdate packages on Debian/Ubuntu linux servers. This allows to run unattended and periodic updates.

## Requirements

None.

## Role Variables

Available variables are listed below, along with default values (see `defaults/main.yml`):

```
autoupdate_enabled: "true"
autoupdate_autofix_interrupted_dpkg: "false"
autoupdate_minimal_steps: "true"
autoupdate_install_on_shutdown: "false"
autoupdate_mail: "root"
autoupdate_mail_only_on_error: "true"
autoupdate_remove_unused_dependencies: "false"
autoupdate_automatic_reboot: "false"
autoupdate_automatic_reboot_time: "02:00"
autoupdate_bandwidth_limit: "70"

autoupdate_periodic_enable: "1"
autoupdate_periodic_update_package_list: "1"
autoupdate_periodic_download_upgradeable_packages: "1"
autoupdate_periodic_unattended_upgrade: "1"
autoupdate_periodic_autoclean_interval: "7"
```

## Dependencies

None.

## Example Playbook

```
- hosts: server
  roles:
    - { role: tschifftner.autoupdate }
```
        
## Supported OS

 - Debian 9 (Stretch)
 - Debian 8 (Jessie)
 - Ubuntu 18.04 (Bionic Beaver)
 - Ubuntu 16.04 (Xenial Xerus)
 
## Required ansible version

Ansible 2.5+

## License

[MIT License](http://choosealicense.com/licenses/mit/)

## Author Information

 - [Tobias Schifftner](https://twitter.com/tschifftner), [ambimax® GmbH](https://www.ambimax.de)