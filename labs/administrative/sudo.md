# Lab: administrative

## File Overview
- **Command:** sudo  
- **Purpose:** Executes a command with elevated (root) privileges without requiring the root password. Instead, it authenticates using the invoking user’s password and permissions defined in /etc/sudoers.

## Observations
Running a command like `sudo apt update` prompted me for **my own** password, not the root password. This is because `sudo` checks whether my user is allowed to run administrative commands based on the `/etc/sudoers` configuration.

I noticed that after entering my password once, I could run additional `sudo` commands for a short period without re‑entering it. This is due to the timestamp timeout feature.

Using `sudo -l` showed me which commands my user is allowed to run. This is useful for verifying permissions without attempting a privileged action.

I also examined `/etc/sudoers` (using `sudo visudo`), which defines rules such as:
- Which users can run which commands  
- Whether a password is required  
- Whether full root privileges are granted or restricted  

`sudo` logs all privileged commands to system logs, providing accountability and traceability.

## Reflection
`sudo` is a safer and more controlled alternative to `su`. Instead of sharing the root password, each user authenticates with their own credentials. This allows administrators to grant limited privileges, audit actions, and reduce the risk of accidental system‑wide damage.

The logging and fine‑grained control make `sudo` essential for multi‑user systems and professional environments. It reinforces the principle of least privilege by allowing users to run only the commands they need, rather than giving them full root access.

Understanding how `sudo` works — and how to configure it properly — is a core skill for Linux administration and is heavily emphasized in real‑world environments.
