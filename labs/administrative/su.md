# Lab: administrative 

## File Overview
- **Command:** su  
- **Purpose:** Allows a user to switch to another user account, most commonly the root account, by providing that user’s password.

## Observations
Running `su` without arguments attempts to switch to the root account. When I entered `su` and provided the root password, the shell prompt changed to indicate that I was now operating as the root user.

Using `su -` (with a hyphen) loads the target user’s full login environment. This includes environment variables, PATH changes, and the user’s default shell. Without the hyphen, `su` switches the user identity but keeps the current environment mostly intact.

I also tested switching to a non‑root user with `su username`. This required that user’s password and changed the shell prompt accordingly.

I entered 'cat /etc/shadow' to view hashed passwords for all account users, a priviledge only a root user can take advantage of.

One important observation is that `su` requires knowing the target user’s password. This makes it less commonly used for administrative tasks on modern systems, where `sudo` is preferred.

## Reflection
`su` is powerful because it gives full access to another user’s account, including root. But that power comes with risk: anyone who knows the root password can gain unrestricted control of the system.

This is why many modern Linux distributions disable the root password by default or encourage using `sudo` instead. `sudo` allows fine‑grained control and auditing, while `su` is all‑or‑nothing.

Still, understanding `su` is important for legacy systems, rescue environments, and situations where root access is required but `sudo` is not configured. It highlights the importance of strong root passwords and careful access control.
