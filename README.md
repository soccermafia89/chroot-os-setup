Role Name
=========

Mounts a boot and root device as a filesystem mount on /mnt.

Requirements
------------

None

Role Variables
--------------

- boot_device_name -- Boot device name, available on /dev/.
- root_device_name: -- Root device name, available on /dev/.
- build_os_distribution: -- OS distribution to install on mounted filesystem.
- build_os_version: -- OS version to install on mounted filesystem.

Dependencies
------------

Example Playbook
----------------

```
- name: Mount Chroot
  hosts: localhost
  roles:
   - chroot-mount
  vars:
    boot_device_name: "sdc"
    root_device_name: "sdd"
    build_os_distribution: "centos"
    build_os_version: "7"
```

License
-------

BSD

Author Information
------------------

Alex Ethier, the Mitre Corporation.
