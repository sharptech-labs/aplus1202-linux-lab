# Lab: common configuration files

## File Overview
- **File:** /etc/resolv.conf  
- **Purpose:** Defines DNS resolver settings, including nameserver IPs and search domains.

## Observations
Output of `cat /etc/resolv.conf`: I observed lines beginning with keywords like `nameserver`, `search`, and `options`.

`nameserver` entries specify the DNS servers the system should query.  
`search` defines domain suffixes that are automatically appended to unqualified hostnames.  
`options` can include settings like timeout values or attempts.

On many modern systems, this file is dynamically managed by services such as NetworkManager or systemd‑resolved, meaning manual edits may be overwritten.

## Reflection
DNS resolution is fundamental to almost everything on a networked system, and `/etc/resolv.conf` is at the heart of that process. Even a small misconfiguration can cause failures in package installation, web browsing, or internal service communication.

It’s also interesting how different Linux distributions handle this file. Some allow direct editing, while others generate it automatically. Understanding how your system manages DNS helps avoid confusion when troubleshooting name resolution issues.
