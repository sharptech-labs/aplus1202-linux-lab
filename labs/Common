# Lab: Common configuration files 

##  File Overview 
-**File:** /etc/passwd  
-**Purpose:** List of registered users and other information such as Username, Group ID, User ID Info, and home directory  
 
##  Observations 
- Output of `cat /etc/passwd`: I observed lines in the /etc/passwd file containing several fields separated by colons. 

  First comes the username, which identifies the account. The second field is usually an x, acting as a placeholder to indicate that the actual password hash is stored securely in /etc/shadow. 

  Next is the user ID (UID), a number that uniquely identifies the user on the system, followed by the group ID (GID), which ties the user to their primary group. After that is the comment field, often used for the full name or a description of the account. 

  The next field specifies the user’s home directory, which is the location they are placed in after logging in. 

  Finally, the last field defines the user’s default shell, such as /bin/bash, which is the program that runs when the user logs in.    

##  Reflection 
- The placeholder (x) for a password on a line is interesting because if it were to be there, since this is not a protected file, it would be suseptable to brute force attacks or dictionary attacks on hashes. 

  Originally, Unix stored password hashes directly in /etc/passwd.

  /etc/passwd must be world‑readable so all programs can look up user information (UIDs, home directories, shells).

  That meant anyone could see the password hashes, making them vulnerable to offline cracking attempts. 

- Password hashes were moved into /etc/shadow, which is restricted to root only.

  /etc/passwd still contains account info, but only a placeholder (x) in the password field.

  /etc/shadow holds the actual hashes, salts, and password aging info.

  This separation ensures that normal users and processes can read account details without exposing sensitive password data.

- This improved security: Only privileged processes can access password hashes.

  It reduced the attack surface by preventing ordinary users from running brute‑force or dictionary attacks on hashes.

 


