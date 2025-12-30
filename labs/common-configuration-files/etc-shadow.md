# Lab: common configuration files

## File Overview
- **File:** /etc/shadow  
- **Purpose:** Stores secure password hashes, salts, and password‑aging information for system accounts. Only root and privileged processes can read it.

## Observations
Output of `sudo cat /etc/shadow`: I observed that each line corresponds to a user account, with fields separated by colons.

The first field is the username.  
The second field contains the hashed password, or a placeholder like `!` or `*` if the account is locked.  
Following that are several fields related to password aging: the last password change date, minimum and maximum password age, warning period, inactivity period, and account expiration date.

The presence of `!` or `*` indicates that the account cannot be used for login. This is common for system accounts.

## Reflection
It makes sense that `/etc/shadow` is heavily restricted. If normal users could read password hashes, even strong hashing algorithms could eventually be brute‑forced.

By separating password hashes into `/etc/shadow`, Unix systems drastically reduce the attack surface. Programs still get user information from `/etc/passwd`, but only privileged processes can access sensitive authentication data.

This design reinforces the principle of least privilege and ensures that password security is not compromised by the need for world‑readable account metadata.
