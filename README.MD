Bash script to automatically mount drives and mountpoints that are defined in
fstab with noauto option.

This is useful for non-critical disks that are not needed to boot, including
external drives and nfs mounts. The script will mount them when the disk / nfs
server is available, and unount when the disk / nfs server is unavailable.
