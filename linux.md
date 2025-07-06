# LINUX TERMINAL COMMANDS

## Table of Contents

- [LINUX TERMINAL COMMANDS](#linux-terminal-commands)
  - [Table of Contents](#table-of-contents)
  - [Keyboard Shortcuts](#keyboard-shortcuts)
  - [Searching](#searching)
  - [Directory Navigation](#directory-navigation)
  - [Packages (Debian/Ubuntu)](#packages-debianubuntu)
  - [Users and Groups](#users-and-groups)
  - [SSH Login](#ssh-login)

## Keyboard Shortcuts

| SHORTCUT | DESCRIPTION                                                                                                          |
| :------- | :------------------------------------------------------------------------------------------------------------------- |
| Ctrl + C | Kill process running in the terminal.                                                                                |
| Ctrl + Z | Stop the current process. The process can be resumed in the foreground with **fg** or in the background with **bg**. |
| Ctrl + W | Cut one word before the cursor and add it to the clipboard.                                                          |
| Ctrl + U | Cut part of the line before the cursor and add it to the clipboard.                                                  |
| Ctrl + K | Cut part of the line after the cursor and add it to the clipboard.                                                   |
| Ctrl + Y | Paste from clipboard.                                                                                                |
| Ctrl + R | Recall the last command that matches the provided characters.                                                        |
| Ctrl + O | Run the previously recalled command.                                                                                 |
| Ctrl + G | Exit command history without running a command.                                                                      |
| clear    | Clear the terminal screen.                                                                                           |
| !!       | Run the last command again.                                                                                          |
| exit     | Log out of the current session.                                                                                      |


## Searching

| COMMAND                                       | DESCRIPTION                                                                                          |
| :-------------------------------------------- | :--------------------------------------------------------------------------------------------------- |
| find [path] -name [search_pattern]            | Find files and directories that match the specified pattern in a specified location.                 |
| find [path] -size [+100M]                     | See files and directories larger than a specified size in a directory.                               |
| grep [search_pattern] [file_name]             | Search for a specific pattern in a file with grep.                                                   |
| grep -r [search_pattern] [directory_name]     | Recursively search for a pattern in a directory.                                                     |
| locate [name]                                 | Locate all files and directories related to a particular name.                                       |
| which [command]                               | Search the command path in the **$PATH** environment variable.                                       |
| whereis [command]                             | Find the source, binary, and manual page for a command.                                              |
| awk '[search_pattern] {print $0}' [file_name] | Print all lines matching a pattern in a file. See also the gawk command, the GNU version of **awk**. |
| sed 's/[old_text]/[new_text]/' [file_name]    | Find and replace text in a specified file.                                                           |

## Directory Navigation

## Packages (Debian/Ubuntu)

## Users and Groups

| COMMAND                              | DESCRIPTION                                                      |
| :----------------------------------- | :--------------------------------------------------------------- |
| id                                   | See details about the active users.                              |
| last                                 | Show the last system logins.                                     |
| who                                  | Display who is currently logged into the system.                 |
| w                                    | Show which users are logged in and their activity.               |
| finger [user_name]                   | Show user information.                                           |
| useradd [user_name]                  | Create a new user account.                                       |
| adduser [user_name]                  | Create a new user account through the adduser command interface. |
| userdel [user_name]                  | Delete a user account.                                           |
| usermod -aG [group_name] [user_name] | Modify user information (add a user to a group).                 |
| passwd                               | Change the current user                                          |
| passwd [user_name]                   | Change another user's password.                                  |
| groupadd [group_name]                | Add a new group.                                                 |
| groupdel [group_name]                | Delete a group.                                                  |
| groupmod -n [new_name] [old_name]    | Modify a user group (change group name).                         |
| sudo [command]                       | Temporarily elevate user privileges to superuser or root.        |
| sudo -i                              | Switch to root user.                                             |
| su - [user_name]                     | Switch the user account or become a superuser.                   |
| chgrp [group_name] [file/directory]  | Change file or directory group.                                  |

## SSH Login
