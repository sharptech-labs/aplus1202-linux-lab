# Lab: text editors

## File Overview
- **Command:** nano  
- **Purpose:** A simple, beginner‑friendly terminal text editor used to create and modify files directly from the command line.

## Observations
Opening a file with `nano filename` launched the editor in the terminal and displayed the file contents along with a helpful menu of shortcuts at the bottom of the screen.

I noticed that navigation is straightforward: the arrow keys move the cursor, and typing inserts text immediately. Unlike more advanced editors, nano does not require switching between modes.

In my wokring directory, /Desktop/labs, I entered 'ls -l' to view my files in that directory. Then, I entered 'nano test4.txt' to edit that file from the command line. I wrote "I added this from nano"

To save my changes, I used:
`Ctrl + O`  
Nano prompted me to confirm the filename, and pressing Enter wrote the changes to disk.

To exit, I used:
`Ctrl + X`  
If there were unsaved changes, nano asked whether I wanted to save before closing.

To check if my edit was successful, I entered 'cat test4.txt and verified the text was added.

I also tested creating a new file simply by running:
`nano newfile.md`  
Nano opened an empty buffer, and saving created the file automatically.

Other useful shortcuts included:
- `Ctrl + K` to cut a line  
- `Ctrl + U` to paste  
- `Ctrl + W` to search within the file  

These shortcuts made editing quick and intuitive.

## Reflection
Nano is ideal for quick edits, configuration changes, and working in minimal environments where graphical editors aren’t available. Its on‑screen shortcut guide makes it approachable even for beginners, and its simplicity reduces the chance of accidental changes or confusion.

Understanding nano is essential for Linux administration because many tasks—especially editing config files—must be done directly in the terminal. Its ease of use and availability on nearly all distributions make it a reliable tool for everyday text editing.
