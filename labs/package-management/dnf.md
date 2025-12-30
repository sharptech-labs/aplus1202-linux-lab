# Lab: package management

## Command overview
- **Command:** dnf  
- **Purpose:** Install, update, upgrade, and remove software packages on RPM-based systems such as Fedora, CentOS Stream, and RHEL.

## Observations
Running `sudo dnf check-update` listed available updates without installing them. This allowed me to see which packages had newer versions before deciding to upgrade.

To install a package, I used:
`sudo dnf install htop`  
Dnf resolved dependencies, downloaded the required packages, and showed a summary of what would be installed before proceeding.

To remove a package, I used:
`sudo dnf remove htop`  
This removed the package and, when appropriate, also removed dependencies that were no longer needed.

I also ran:
`sudo dnf upgrade`  
This upgraded installed packages to their latest versions from the configured repositories.

Using:
`sudo dnf history`  
showed a list of past transactions, including installs, upgrades, and removals. This made it easier to review what had changed on the system.

## Reflection
Dnf provides detailed transaction information and good dependency handling, which makes it a powerful package manager for RPM-based systems. The history feature is especially useful for troubleshooting or understanding what changed after an update.

Knowing how to use `dnf install`, `dnf remove`, `dnf upgrade`, and `dnf history` is important for managing software effectively on Fedora and other RPM-based distributions.
