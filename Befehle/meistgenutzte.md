# Meistgenutzte

- [1. `ls`: List directory contents.](#1-ls-list-directory-contents)
- [2. `cd`: Change directory.](#2-cd-change-directory)
- [3. `pwd`: Print working directory.](#3-pwd-print-working-directory)
- [4. `mkdir`: Make directory.](#4-mkdir-make-directory)
- [5. `rm`: Remove files or directories.](#5-rm-remove-files-or-directories)
- [6. `cp`: Copy files and directories.](#6-cp-copy-files-and-directories)
- [7. `mv`: Move or rename files and directories.](#7-mv-move-or-rename-files-and-directories)
- [8. `touch`: Create an empty file.](#8-touch-create-an-empty-file)
- [9. `cat`: Concatenate and display file content.](#9-cat-concatenate-and-display-file-content)
- [10. `grep`: Search for patterns in files.](#10-grep-search-for-patterns-in-files)
- [11. `chmod`: Change file permissions.](#11-chmod-change-file-permissions)
- [12. `chown`: Change file ownership.](#12-chown-change-file-ownership)
- [13. `sudo`: Execute a command as a superuser (root).](#13-sudo-execute-a-command-as-a-superuser-root)
- [14. `apt-get` or `apt`: Package management command for Debian-based systems.](#14-apt-get-or-apt-package-management-command-for-debian-based-systems)
- [15. `yum`: Package management command for RPM-based systems.](#15-yum-package-management-command-for-rpm-based-systems)
- [16. `ssh`: Secure Shell client for remote login.](#16-ssh-secure-shell-client-for-remote-login)
- [17. `wget`: Download files from the web.](#17-wget-download-files-from-the-web)
- [18. `top`: Display system resource usage.](#18-top-display-system-resource-usage)
- [19. `ps`: List running processes.](#19-ps-list-running-processes)
- [20. `kill`: Terminate a process.](#20-kill-terminate-a-process)
- [21. `find`: Search for files and directories.](#21-find-search-for-files-and-directories)
- [22. `history`: View command history.](#22-history-view-command-history)

> First off all I want to mention that you can show all OPTIONS and help with `command -h` or `command --help`. Of course switch command with for example ls: `ls --help`.

## 1. `ls`: List directory contents.

- Description: Lists the files and directories in the current directory.
- Syntax: `ls [OPTIONS] [FILE]`
- Example: `ls -a` Lists files and directories in the current directory. With the `-a` it even shows hidden items

- Example: `ls -t` Lists files and directories in the current directory. With the `-t` it sorts it by time and date

Read more about it in [\*](*)

## 2. `cd`: Change directory.

- Description: Changes the current working directory.
- Syntax: `cd [OPTIONS] [DIRECTORY]`
- Example: `cd /bbw-linux-cookbook` your now working in the bbw-linux-cookbook directory

- Example: `cd /Users/pascal/Desktop ` changes to the desktop of the user pascal

Read more about it in [\*](*)

## 3. `pwd`: Print working directory.

- Description: Displays the current working directory path.
- Syntax: `pwd [OPTIONS]`
- Example: `pwd` will just print you your current path for example: `/Users/pascal`

Read more about it in [\*](*)

## 4. `mkdir`: Make directory.

- Description: Creates a new directory. (If it doesn't exist)
- Syntax: `mkdir [OPTIONS] DIRECTORY`
- Example: `mkdir bbw-linux-cookbook` (creates a directory named "bbw-linux-cookbook" in the current directory)

> If you want to combine it with cd and ls you can enter `mkdir bbw-linux-cookbook && cd bbw-linux-cookbook`

Read more about it in [\*](*)

## 5. `rm`: Remove files or directories.

- Description: Deletes files or directories. (Without any OPTION rm wont remove files)
- Syntax: `rm [OPTIONS] FILE/DIRECTORY`
- Example: `rm -r bbw-linux-cookbook` (removes the file "bbw-linux-cookbook.txt")
- Example: `rm -rf text.txt` (removes the file even it its in use)

Read more about it in [\*](*)

## 6. `cp`: Copy files and directories.

- Description: Copies files or directories to a new location.
- Syntax: `cp [OPTIONS] SOURCE DESTINATION`
- Example: `cp text.txt mostUsed.txt` (copies "text.txt" and names the copy "mostUsed.txt")
- Example: `cp text.txt bbw-linux-cookbook/mostUsed.txt` (copies "text.txt" and names the copy "mostUsed.txt")

Read more about it in [\*](*)

## 7. `mv`: Move or rename files and directories.

- Description: Moves or renames files and directories.
- Syntax: `mv [OPTIONS] SOURCE DESTINATION`
- Example: `mv mostUsed.txt bbw-linux-cookbook/` (moves "text.txt" to the directory "bbw-linux-cookbook/")

Read more about it in [\*](*)

## 8. `touch`: Create an empty file.

- Description: Creates a new empty file.
- Syntax: `touch [OPTIONS] FILENAME`
- Example: `touch mostUsed.txt` (creates a new empty file named "mostUsed.txt" in the current directory)
- Example: `touch mostUsed1.txt mostUsed2.txt mostUsed3.txt` (creates three files in the working directory)

Read more about it in [\*](*)

## 9. `cat`: Concatenate and display file content.

- Description: Displays the content of a file.
- Syntax: `cat [OPTIONS] FILENAME`
- Example: `cat mostUsed.txt` (displays the content of "mostUsed.txt")

- Example: `cat mostUsed1.txt mostUsed2.txt mostUsed3.txt` (displays the content of those three files)

Read more about it in [\*](*)

## 10. `grep`: Search for patterns in files.

- Description: Searches for a specific pattern in files.
- Syntax: `grep [OPTIONS] PATTERN FILENAME`
- Example: `grep "keyword" mostUsed.txt` (searches for the word "keyword" in "mostUsed.txt")
- Example: `grep --color "keyword" mostUsed.txt` (searches for the word "keyword" in "mostUsed.txt" and then colors it)

> You can use REGEX to search with grep. Learn about this: [www.digitalocean.com](https://www.digitalocean.com/community/tutorials/grep-command-in-linux-unix#using-grep-with-regual-expressions-regex)

Read more about it in [\*](*)

## 11. `chmod`: Change file permissions.

- Description: Modifies the permissions of a file or directory.
- Syntax: `chmod [OPTIONS] MODE FILE/DIRECTORY`
- Example: `chmod rwx mostUsed.txt` (changes the permissions of "mostUsed.txt" to full permissions)
- - Example: `chmod --- mostUsed.txt` (changes the permissions of "mostUsed.txt" to zero permissions)

Read more about it in [\*](*)

## 12. `chown`: Change file ownership.

- Description: Changes the owner and group of a file or directory.
- Syntax: `chown [OPTIONS] USER[:GROUP] FILE(s)`
- Example: `chown pascal mostUsed.txt` (changes the owner of "mostUsed.txt" to the user pascal)

Read more about it in [\*](*)

## 13. `sudo`: Execute a command as a superuser (root).

- Description: Runs a command with administrative privileges.
- Syntax: `sudo [OPTIONS] COMMAND`

Read more about it in [\*](*)

## 14. `apt-get` or `apt`: Package management command for Debian-based systems.

- Description: Manages software packages on Debian-based systems.
- Syntax: `apt-get [OPTIONS] COMMAND` or `apt [OPTIONS] COMMAND`
- Example: `apt-get install vim` (installs vim using apt-get)
  Read more about it in [\*](*)

## 15. `yum`: Package management command for RPM-based systems.

- Description: Manages software packages on RPM-based systems.
- Syntax: `yum [OPTIONS] COMMAND`
- Example: `yum install vsftpd` (installs the vsftpd package using yum)

Read more about it in [\*](*)

## 16. `ssh`: Secure Shell client for remote login.

- Description: Connects to a remote server via SSH.
- Syntax: `ssh [OPTIONS] [USER@]HOST`
- Example: `ssh pascal@10.143.90.2` (connects to "10.143.90.2" with the specified username)

Read more about it in [\*](*)

## 17. `wget`: Download files from the web.

- Description: Downloads files from the internet.
- Syntax: `wget [OPTIONS] URL`
- Example: `wget[ http://example.com/file.txt](https://filesamples.com/samples/image/png/sample_640%C3%97426.png)` (downloads the image from the specified URL)
  Read more about it in [\*](*)

## 18. `top`: Display system resource usage.

- Description: Shows real-time information about system resource usage.
- Syntax: `top [OPTIONS]`
- Example: `top` (displays real-time system resource usage)

Read more about it in [\*](*)

## 19. `ps`: List running processes.

- Description: Displays the running processes on the system.
- Syntax: `ps [OPTIONS]`
- Example: `ps aux` (lists all running processes with detailed information)

Read more about it in [\*](*)

## 20. `kill`: Terminate a process.

- Description: Terminates a running process.
- Syntax: `kill [OPTIONS] PID`
- Example: `kill 1234` (terminates the process with ID 1234)

Read more about it in [\*](*)

## 21. `find`: Search for files and directories.

- Description: Searches for files and directories based on specified criteria.
- Syntax: `find [OPTIONS] [PATH] [CRITERIA]`
- Example: `find pascal/bbw-linux-cookbook/user -name "*.txt"` (searches for all files with the .txt extension in the /pascal/bbw-linux-cookbook directory)

Read more about it in [\*](*)

## 22. `history`: View command history.

- Description: Displays the command history of the current session.
- Syntax: `history [OPTIONS]`
- Example: `history` (displays the command history)

Read more about it in [\*](*)
