## Ansible Role: common
Common setup tasks for all RedHat/CentOS 7 servers

## Tasks
* Enable SELinux (immediate reboot to activate)
* Add swap (otherwise a small VPS may be visited by the OOM Killer in later tasks)
* Enable firewalld
* Create initial users (ssh keys, sudo access)
* Harden sshd configuration
  * Disable root login
  * Disable password authentication
  * Move to non-default port (also handles SELinux & firewalld config for this)
* Update all existing packages
* Install user-defined base packages (ex: vim, unzip)
* Enable auto-updates (via yum-cron)
* Install global shell enhancements (custom aliases, vim configs)
* Set timezone

## License
2-clause BSD
