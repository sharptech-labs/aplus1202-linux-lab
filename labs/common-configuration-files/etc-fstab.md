# Lab: common configuration files

## File Overview
- **File:** /etc/ffstab  
- **Purpose:** Defines filesystems and mount points that should be automatically mounted at boot.

## Observations
Output of `cat /etc/fstab`: I observed a table‑like structure where each line represents a filesystem. Fields are separated by spaces or tabs.

The first field is the device or UUID.  
The second field is the mount point (e.g., `/`, `/home`, `/boot`).  
The third field specifies the filesystem type, such as ext4, xfs, or swap.  
The fourth field lists mount options like `defaults`, `noatime`, or `rw`.  
The last two fields control dump behavior and filesystem checks during boot.

The use of UUIDs instead of device names helps ensure consistent mounting even if device ordering changes.

## Reflection
`/etc/fstab` is one of those files where a single typo can prevent a system from booting properly. It highlights how critical accurate configuration is in Linux administration.

The structure is simple, but the impact is huge: it determines what storage is available, how it’s mounted, and whether the system can even start. Understanding this file is essential for managing disks, partitions, and persistent storage.
