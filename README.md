# Ansible Role: Prepare backup sources for remote rsync over SSH

This role prepares a host to be part of a backup solution. Backup source directories are configured, which will be used by the controller rules

https://github.com/andreasbehnke/ansible-role-usb-disk-backup
https://github.com/andreasbehnke/ansible-role-scheduled-backup

## Backup Sources
Each backup source must provide the following variables:

```
backup_sources:
    - path: "/path/to/files"
      rsync_opts: "-aRH --exclude='lost+found' ..."
      user: "username"
      group: "goupname"
    - path: ...
```

