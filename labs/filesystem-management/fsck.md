# Lab: filesystem management

## File Overview
- **Command:** fsck
- **Purpose:** Checks and repairs filesystem inconsistencies. Typically used after improper shutdowns, disk corruption, or when the system detects filesystem errors.

## Observations
Running `fsck` without specifying a device resulted in a warning, reminding me that the command must be run on an unmounted filesystem. This makes sense because modifying a live, mounted filesystem can cause further corruption.

When I ran `sudo fsck /dev/sda1` on a test partition, the tool scanned the filesystem and reported issues such as orphaned inodes or incorrect block counts. It prompted me to confirm fixes one by one unless I used the `-y` option to automatically repair everything.

I also noticed that different filesystem types use different backend tools:
- ext4 uses `e2fsck`
- xfs uses `xfs_repair` (and does not support fsck directly)
- FAT filesystems use `fsck.vfat`

The output clearly indicated the pass number, the type of check being performed, and whether the filesystem was clean or required repairs.

## Reflection
`fsck` is one of those commands that can save a system from serious issues, but it must be used carefully. Running it on a mounted filesystem can cause more harm than good, which is why systems often run fsck automatically during boot before mounting partitions.

It highlights how important filesystem integrity is for Linux systems. Even small inconsistencies can lead to data loss or boot failures. Understanding when and how to use `fsck` is essential for troubleshooting storage issues and maintaining system reliability.
