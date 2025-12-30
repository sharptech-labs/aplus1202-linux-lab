# Lab: filesystem management

## File Overview
- **Command:** mount
- **Purpose:** Attaches a filesystem to a directory (mount point) so it becomes accessible to the system.

## Observations
Running `mount` with no arguments displayed a list of all currently mounted filesystems. Each entry showed the device, the mount point, the filesystem type, and the mount options. This provided a clear snapshot of how storage is currently organized on the system.

To manually mount a device, I used:
`sudo mount /dev/sdb1 /mnt`
After running this, the contents of the device became available under `/mnt`.

I also tested specifying the filesystem type explicitly with:
`sudo mount -t ext4 /dev/sdb1 /mnt`
This can be useful when the filesystem type is not automatically detected or when I want to be explicit.

The `mount` command supports many useful options, such as:
- `ro` for read‑only access
- `rw` for read‑write
- `noexec` to prevent running binaries from that filesystem
- `nosuid` to ignore setuid bits

To detach a filesystem, I used the `umount` command:
`sudo umount /mnt`
If the filesystem was still in use, `umount` warned that the target was busy, which helps prevent data loss or corruption.

## Reflection
The `mount` command is fundamental to how Linux works with storage. Instead of assigning drive letters like Windows, Linux attaches filesystems anywhere within a single directory tree, which is very flexible but requires understanding mount points.

Being comfortable with `mount` and `umount` is essential for managing external drives, troubleshooting disk issues, and working in recovery or rescue environments. Combined with `/etc/fstab`, which automates mounting at boot, these tools form a core part of Linux file management and system administration.
