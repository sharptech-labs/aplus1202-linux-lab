# Lab: package management

## Command overview
- **Command:** apt  
- **Purpose:** Install, update, upgrade, and remove software packages on Debian-based systems such as Ubuntu and Linux Mint.

## Observations
Running `sudo apt update` refreshed the local package index by downloading the latest lists of available software from the configured repositories. This did not install or upgrade anything; it only updated information about what versions are available.

After that, running `sudo apt upgrade` compared installed packages with the updated index and offered to upgrade any outdated packages. The command showed how many packages would be upgraded and how much additional disk space would be used before asking for confirmation.

I installed Wireshark by entering 'sudo apt install wireshark'. It prompted me for my password as this is an elevated rights command, it specified how much disk space would be used, then I continued with the installation process.

## Reflection
Apt makes managing software straightforward by separating the steps of updating the package index and upgrading packages. Its automatic dependency handling and clear prompts make it easier to avoid mistakes while maintaining the system.

Understanding how to use `apt update`, `apt upgrade`, `apt install`, `apt remove`, and `apt purge` is essential for keeping Debian-based systems up to date, secure, and free of unnecessary software.
