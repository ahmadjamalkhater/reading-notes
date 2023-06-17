# Command Line Tutorial for Linux - Part 1: Basics

## Summary

This tutorial aims to explain the usage of the command line interface in Linux. It covers the fundamental concepts and provides step-by-step instructions for each process. The focus is on helping users confidently navigate and utilize the command line interface efficiently.

## Included Shortcuts

### Opening the command line window:

- **macOS**: Search for the Terminal program under Applications -> Utilities. Alternatively, use the `command + space` keys to open Spotlight and search for Terminal.
- **Linux**: Find the command line interface under Applications -> System or Applications -> Utilities. You can also right-click on the desktop and select "Open in terminal."
- **Windows**: To remotely log into another machine, you need an SSH client like Putty (free).

### Understanding the Shell (Bash):

Within the terminal, there is a shell that determines the behavior of the interface and executes commands. The most commonly used shell in Linux is Bash (Bourne again shell). To check the current shell, use the `echo $SHELL` command, which should display `/bin/bash` or similar.

### Shortcuts:

The terminal provides various shortcuts to enhance productivity and avoid mistakes. Here are some useful ones:

- **Command History**: Use the up and down arrow keys to browse through previously entered commands.
- **Command Editing**: Use the left and right arrow keys to move the cursor within a command and make edits.


---


# Linux Tutorial - 2. Navigation

Introduction:
In this tutorial, we will cover the basics of navigating through the Linux system. Being able to move around and reference the correct locations is crucial for effective work in Linux. It is important to thoroughly understand these concepts.

1. Finding the Current Location:
The first command we will learn is `pwd`, which stands for "Print Working Directory". This command displays the current working directory. Use it to find out where you are in the system.
Example:
pwd
/home/ryan
It is easy to lose track of your location while navigating, so use the `pwd` command frequently to remind yourself.

2. Listing Contents:
To see what is in the current location, we use the `ls` command, which stands for "list". It provides a listing of files and directories in the specified location.
Example:
ls
bin Documents public_html
The `ls` command can be customized with options and arguments. Here is an outline of its usage:
ls [options] [location]
In the above example, the square brackets indicate optional items. You can run the command with or without them. Here are some variations:
ls
bin Documents public_html

ls -l
total 3
drwxr-xr-x 2 ryan users 4096 Mar 23 13:34 bin
drwxr-xr-x 18 ryan users 4096 Feb 17 09:12 Documents
drwxr-xr-x 2 ryan users 4096 May 05 17:25 public_html

ls /etc
a2ps.cfg aliases alsa.d cups fonts my.conf systemd

ls -l /etc
total 3
-rwxr-xr-x 2 root root 123 Mar 23 13:34 a2ps.cfg
-rwxr-xr-x 18 root root 78 Feb 17 09:12 aliases
drwxr-xr-x 2 ryan users 4096 May 05 17:25 alsa.d

3. Paths:
Paths are used to specify the location of a file or directory on the command line. There are two types of paths: absolute and relative.
- Absolute paths: Specify a location in relation to the root directory ("/").
- Relative paths: Specify a location in relation to the current directory.
Examples:
pwd
/home/ryan

ls Documents
file1.txt file2.txt file3.txt

ls /home/ryan/Documents
file1.txt file2.txt file3.txt

4. Moving Around:
To navigate through directories, we use the `cd` command, which stands for "change directory". It allows you to change your current location.
Examples:
pwd
/home/ryan

cd Documents
ls
file1.txt file2.txt file3.txt

cd /
pwd
/
ls
bin boot dev etc home lib var

cd ~/Documents
pwd
/home/ryan/Documents

cd ../../
pwd
/home

cd
pwd
/home/ryan

5. Tab Completion:
Tab Completion is a helpful feature in the command line that auto-completes paths and commands as you type. Pressing the Tab key invokes auto-completion, and if there are multiple possibilities, pressing Tab again displays them.

6. Summary:
- `pwd`: Print the current working directory.
- `ls`: List the contents of a directory

Linux Tutorial - 5 .Cheat Sheet

Overview:
This cheat sheet provides a concise summary of essential commands and concepts for navigating and working with Linux. It serves as a handy reference for quick reminders and is intended for users who are already familiar with the Linux command line.

Basic Navigation:
- `pwd`: Print current working directory.
- `ls`: List files and directories.
- `cd`: Change directory.

Path:
- Absolute Path: Starts from the root directory.
- Relative Path: Relative to the current directory.
- `~` (tilde): Represents the home directory.
- `.` (dot): Represents the current directory.
- `..` (dot dot): Represents the parent directory.

TAB Completion:
- Auto-completes paths and commands.

More About Files:
- `file`: Identify file or directory type.
- Handling spaces in names.
- Hidden files and directories.
- Permissions: `r` (read), `w` (write), `x` (execute).

Process Management:
- `CTRL + C`: Cancel the current process.
- `kill`: Terminate a process.
- `ps`: List processes.
- `CTRL + Z`: Pause a process and put it in the background.
- `jobs`: List background processes.
- `fg`: Bring a background process to the foreground.

Manual Pages:
- `man`: Access command documentation.

Vi / Vim:
- Text editor commands.

Filters:
- `head`: Display the first lines of a file.
- `tail`: Display the last lines of a file.
- `sort`: Sort lines in a file.
- `wc`: Count words, characters, and lines.
- `grep`: Search for patterns in a file.

Useful Commands:
- `du`: Find directory sizes.
- `df`: Display disk space usage.
- `mkdir`: Create a directory.
- `rmdir`: Remove an empty directory.
- `touch`: Create an empty file.
- `cp`: Copy files and directories.
- `mv`: Move or rename files and directories.
- `rm`: Remove files and directories.
- Wildcards: `*`, `?`, `[]`.

Piping and Redirection:
- `>`: Redirect STDOUT to a file.
- `>>`: Append STDOUT to a file.
- `2>`: Redirect STDERR to a file.
- `<`: Pass file contents as STDIN.
- `|`: Pipe STDOUT of one command to another.

Note: This cheat sheet provides a summary of the main concepts and commands. For detailed explanations and examples, refer to the tutorial pages.

By Ryan Chadwick © 2023

---
# More About Files-3

## Linux Files: A Summary
## Main Points

1. **Everything is a File:**
   - All entities in Linux, such as text files, directories, keyboards, and monitors, are treated as files.
   - Understanding this concept is crucial for effective file and directory management.

2. **Linux is Extensionless:**
   - Unlike Windows, Linux does not rely on file extensions to determine file types.
   - Linux looks inside the file content to identify its type.
   - The `file` command can be used to determine the file type.

3. **Linux is Case Sensitive:**
   - Linux considers letter case when referring to files and directories.
   - Files with the same name but different case are treated as separate entities.
   - Pay attention to accurately specify the case when working with files and directories.

4. **Dealing with Spaces in Names:**
   - Spaces in file and directory names are valid but require special handling on the command line.
   - Two approaches can be used to handle spaces:
     - Quotes: Enclose the entire name in single (`'`) or double (`"`) quotes as a single item.
     - Escape Characters: Place a backslash (`\`) before the space to nullify its special meaning.

5. **Hidden Files and Directories:**
   - Linux allows files and directories to be hidden by starting their names with a dot (`.`).
   - Hidden files are not listed by default in directory listings.
   - Use the `ls` command with the `-a` option to display hidden files and directories.

## Steps for Practice

To gain a better understanding of working with files in Linux, follow these steps:

1. Use the `file` command with various entries, including absolute and relative paths, to determine file types.
2. List the contents of your home directory, including hidden files and directories, using the appropriate command.

Refer back to these main points and follow the suggested steps to enhance your proficiency in managing files in Linux.

---

# Title: "Linux Tutorial - 4. Manual Pages: A Summary"
Main Points:

Introduction:
- The Linux command line provides immense power and opportunities.
- Manual pages serve as a comprehensive resource for understanding command line operations.

Manual Pages:
- Manual pages explain every command on the system, including their functions, usage, and command line arguments.
- They can be accessed using the "man" command followed by the desired command name.

Structure of Manual Pages:
- The manual pages consist of several sections:
    1. Command name and a brief description.
    2. Synopsis: A quick overview of how the command should be run.
    3. Detailed description of the command's functionality.
    4. Command line options and arguments.
- To exit the manual pages, press 'q'.

Searching:
- Keyword search: Use the "man -k" command followed by the search term to find relevant manual pages.
- Search within a manual page: While viewing a specific manual page, press '/' followed by the search term and press 'enter'.

Running Commands:
- Commands have both long and short options.
- Long options begin with two dashes (e.g., "--all"), while short options start with a single dash (e.g., "-a").
- Short options can be combined together after a single dash.
- Long options provide better readability, while short options allow for easier chaining of multiple options.

Summary of Commands:
- "man <command>": Look up the manual page for a specific command.
- "man -k <search term>": Perform a keyword search across all manual pages.
- "/<term>": Search within a manual page for a particular term.
- "n": Navigate to the next occurrence of a search term within a manual page.

Activities:
- Skim through the "ls" manual page and experiment with different command line options.
- Conduct searches within the manual pages to explore various topics and commands.

By Ryan Chadwick © 2023

---
# "Linux Tutorial - 5. File Manipulation"
1. List files and directories: `ls`
   Example: `ls`
   This command will list all files and directories in the current directory.

2. Change directory: `cd <directory path>`
   Example: `cd documents`
   This command will change the current directory to the specified directory.

3. Create a file: `touch <filename>`
   Example: `touch file.txt`
   This command will create a new file with the specified name.

4. Copy a file: `cp <source> <destination>`
   Example: `cp file.txt backup/file.txt`
   This command will copy the file from the source location to the destination location.

5. Move or rename a file: `mv <source> <destination>`
   Example: `mv file.txt documents/file_new.txt`
   This command will move the file from the source location to the destination location or rename the file.

6. Remove a file: `rm <filename>`
   Example: `rm file.txt`
   This command will delete the specified file.

7. Remove an empty directory: `rmdir <directory>`
   Example: `rmdir documents`
   This command will remove the specified empty directory.

8. Remove a directory and its contents: `rm -r <directory>`
   Example: `rm -r documents`
   This command will remove the specified directory and its contents. Be careful when using this command as it doesn't ask for confirmation and deletes the directory immediately.

9. View the contents of a text file: `cat <filename>`
   Example: `cat file.txt`
   This command will display the contents of the text file on the screen.

10. Edit a text file: `nano <filename>`
    Example: `nano file.txt`
    This command will open the text file in the nano editor, allowing you to edit it and save the changes.

These are some basic commands that you can use to manage files and directories in the operating system. You can explore more commands and options by reading the documentation of your operating system or referring to tutorials and online resources.

---

Linux Tutorial - Cheat Sheet

Overview:
This cheat sheet provides a concise summary of essential commands and concepts for navigating and working with Linux. It serves as a handy reference for quick reminders and is intended for users who are already familiar with the Linux command line.

Basic Navigation:
- `pwd`: Print current working directory.
- `ls`: List files and directories.
- `cd`: Change directory.

Path:
- Absolute Path: Starts from the root directory.
- Relative Path: Relative to the current directory.
- `~` (tilde): Represents the home directory.
- `.` (dot): Represents the current directory.
- `..` (dot dot): Represents the parent directory.

TAB Completion:
- Auto-completes paths and commands.

More About Files:
- `file`: Identify file or directory type.
- Handling spaces in names.
- Hidden files and directories.
- Permissions: `r` (read), `w` (write), `x` (execute).

Process Management:
- `CTRL + C`: Cancel the current process.
- `kill`: Terminate a process.
- `ps`: List processes.
- `CTRL + Z`: Pause a process and put it in the background.
- `jobs`: List background processes.
- `fg`: Bring a background process to the foreground.

Manual Pages:
- `man`: Access command documentation.

Vi / Vim:
- Text editor commands.

Filters:
- `head`: Display the first lines of a file.
- `tail`: Display the last lines of a file.
- `sort`: Sort lines in a file.
- `wc`: Count words, characters, and lines.
- `grep`: Search for patterns in a file.

Useful Commands:
- `du`: Find directory sizes.
- `df`: Display disk space usage.
- `mkdir`: Create a directory.
- `rmdir`: Remove an empty directory.
- `touch`: Create an empty file.
- `cp`: Copy files and directories.
- `mv`: Move or rename files and directories.
- `rm`: Remove files and directories.
- Wildcards: `*`, `?`, `[]`.

Piping and Redirection:
- `>`: Redirect STDOUT to a file.
- `>>`: Append STDOUT to a file.
- `2>`: Redirect STDERR to a file.
- `<`: Pass file contents as STDIN.
- `|`: Pipe STDOUT of one command to another.

Note: This cheat sheet provides a summary of the main concepts and commands. For detailed explanations and examples, refer to the tutorial pages.

By Ryan Chadwick © 2023


