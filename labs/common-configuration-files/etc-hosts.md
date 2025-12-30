# Lab: common configuration files

## File Overview
- **File:** /etc/hosts  
- **Purpose:** Provides static hostname‑to‑IP address mappings. Used before DNS queries and useful for local overrides or testing.

## Observations
Output of `cat /etc/hosts`: I observed a simple list of IP addresses paired with hostnames. The most common entries include `127.0.0.1` mapped to `localhost`, and sometimes IPv6 equivalents like `::1`.

Each line contains an IP address followed by one or more hostnames or aliases. The file is processed from top to bottom, and entries here take precedence over DNS.

This file is often used for local development, blocking domains, or forcing a hostname to resolve to a specific IP.

## Reflection
It’s interesting how such a small file can override DNS entirely. This gives administrators a powerful tool for troubleshooting or controlling name resolution behavior.

Because `/etc/hosts` is read before DNS, it can be used to redirect traffic, test new servers, or isolate systems during migrations. It’s a reminder that even simple text files can play a critical role in networking and system behavior.
