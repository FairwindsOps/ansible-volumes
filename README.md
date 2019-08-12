Volumes
=========

This role mounts devices and ensures filesystems on the devices.

It spins through all mount points described in the `volumes_mounts` variable.

Role Variables
--------------

`volumes_mounts`

Example:

```
volumes_mounts:
  - device_path: "/dev/xvdb"
   file_path: "/ssd"
   filesystem: "ext4"
   mount_opts: "noatime,nodiratime"
   mount_state: "mounted"
  - device_path: "/dev/xvdf"
   file_path: "/data"
   filesystem: "ext4"
   mount_opts: "noatime,nodiratime"
   mount_state: "mounted"
```

Example Playbook
----------------

Use this role by populating `volume_mounts` and including the role:

```
    - hosts: servers
      roles:
         - { role: fairwinds.volumes }
```
