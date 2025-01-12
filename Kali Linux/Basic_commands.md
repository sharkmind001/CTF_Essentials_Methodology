# Basic Linux Commands

## Create Files


| **Command**                                                        | **Description**                                                                                  |
|--------------------------------------------------------------------|--------------------------------------------------------------------------------------------------|
| `touch abc.txt`                                                    | Create a file named `abc.txt`.                                                                  |
| `touch abc1 abc2 abc3`                                             | Create multiple files named `abc1`, `abc2`, and `abc3`.                                         |
| `touch amit /deepak /tmp/xyz`                                      | Create files in different locations at the same time.                                           |
| `touch notes{1,2,3}`                                               | Create multiple files named `notes1`, `notes2`, and `notes3`.                                   |
| `touch notes{a,bc,}`                                               | Create multiple files with names such as `notesa`, `notesbc`, and `notes`.                      |
| `touch ibm{1..5}`                                                  | Create 5 files named `ibm1` to `ibm5`.                                                          |
| `touch ibm{0..20}`                                                 | Create 21 files named `ibm0` to `ibm20`.                                                        |
| `touch redhat{0..20..2}`                                           | Create files in an even-numbered series (e.g., `redhat0`, `redhat2`, ..., `redhat20`).          |
| `touch rajeev{1..5}.txt`                                           | Create files with `.txt` extension named `rajeev1.txt` to `rajeev5.txt`.                        |
| `touch /tmp/my-public-data/abc{1..5}`                              | Create files named `abc1` to `abc5` in the `/tmp/my-public-data/` directory.                    |
| `ls /tmp/my-public-data/`                                          | List the files created in the `/tmp/my-public-data/` directory.                                 |


## Create Directory

| **Command**                                       | **Description**                                                                                  |
|---------------------------------------------------|--------------------------------------------------------------------------------------------------|
| `mkdir dir1`                                      | Create a directory named `dir1`.                                                                |
| `mkdir dir1 dir2`                                 | Create multiple directories named `dir1` and `dir2`.                                            |
| `mkdir new\ folder`                               | Create a directory with a space in its name (e.g., `new folder`).                               |
| `mkdir my\ home\ directory`                       | Create a directory named `my home directory` using backslashes to escape spaces.                |
| `mkdir 'new folder'`                              | Create a directory named `new folder` using single quotes.                                      |
| `mkdir "new folder"`                              | Create a directory named `new folder` using double quotes.                                      |
| `mkdir -p /data/a1/a2/a3/a4/a5`                   | Create a directory with sub-directories in a single command.                                    |
| `cd data`                                         | Change to the `data` directory.                                                                 |
| `cd /data/a2/a3/a4/`                              | Change directories through multiple levels.                                                     |
| `cp /home/kali/Desktop/notes.txt .`               | Copy the file `notes.txt` from the desktop to the current directory.                            |
| `mv /tmp/abc.txt /home/kali/`                     | Move the file `abc.txt` from `/tmp` to `/home/kali/`.                                           |

## Zip and Unzip Files

| **Command**                                       | **Description**                                                                                  |
|---------------------------------------------------|--------------------------------------------------------------------------------------------------|
| `zip compress.zip <file1 file2 file3>`            | Compress multiple files into a zip archive named `compress.zip`.                                |
| `zip ravi.zip notes.txt mynote2.txt`              | Compress specific files into a zip archive.                                                     |
| `zip ravi.zip *.txt`                              | Compress all files with the `.txt` extension.                                                   |
| `zip ravi.zip *`                                  | Compress all files in the current directory.                                                    |
| `zip -v ravi.zip *`                               | Compress all files with verbose output.                                                         |
| `zip -r compress.zip <folder_name>`               | Compress an entire folder (directory).                                                          |
| `zip -r compress.zip Myfiles`                     | Compress the folder named `Myfiles`.                                                            |
| `unzip compress.zip`                              | Extract the contents of the zip archive.                                                        |
| `unzip compress.zip /home/user/kali/`             | Extract the zip archive to a specific folder.                                                   |
| `unzip -P your-password zipfile.zip`              | Extract a password-protected zip archive.                                                       |

## Tar and Gzip Files

| **Command**                                       | **Description**                                                                                  |
|---------------------------------------------------|--------------------------------------------------------------------------------------------------|
| `tar -cf myfiles.tar file1 file2`                 | Create a `.tar` archive containing `file1` and `file2`.                                          |
| `tar -cf myfolder.tar myfolder1`                  | Create a `.tar` archive of a folder.                                                            |
| `tar -xvf myfiles.tar`                            | Extract files from a `.tar` archive.                                                            |
| `tar -cf myfiles.tar myfiles/`                    | Create a `.tar` archive of the folder `myfiles/`.                                               |
| `gzip myfiles.tar`                                | Compress a `.tar` file to create a `.tar.gz` file.                                              |
| `tar -zxvf myfiles.tar.gz`                        | Extract files from a `.tar.gz` archive.                                                         |

There are some more zip files.

`.gzip`
`.lzma`
`.bzip2`
`.7z`

## Rename Files and Folders

| **Command**                                      | **Description**                                                                         |
|--------------------------------------------------|-----------------------------------------------------------------------------------------|
| `mv <old_name> <new_name>`                       | Rename a single file.                                                                  |
| `mv ca.zip da.zip`                               | Rename a file from `ca.zip` to `da.zip`.                                               |
| `mv <old_dir_name> <new_dir_name>`               | Rename a directory.                                                                    |
| `mv temp myfiles`                                | Rename the directory `temp` to `myfiles`.                                              |
| `rename 's/old-name/new-name/' files`            | Rename a large group of files using a pattern.                                         |
| `rename 's/\.txt$/\.pdf/' *.txt`                 | Convert all `.txt` files to `.pdf` files.                                              |

## Delete Files and Folders

| **Command**                                      | **Description**                                                                         |
|--------------------------------------------------|-----------------------------------------------------------------------------------------|
| `unlink file1 file2`                             | Delete a single file using `unlink`.                                                   |
| `rm file1 file2`                                 | Remove individual files.                                                               |
| `rm -i mydir/*`                                  | Delete all files in the `mydir` directory, one by one, with confirmation for each.      |
| `rm -f filename`                                 | Remove files without prompting, even if they are write-protected.                      |
| `rm -fv *.txt`                                   | Delete `.txt` files forcefully and verbosely.                                          |
| `rmdir dirname`                                  | Delete an empty directory.                                                             |
| `rm -d dirname`                                  | Delete an empty directory.                                                             |
| `rm -r dirname`                                  | Delete a non-empty directory and all files within it recursively.                      |
| `rm -rf dirname`                                 | Forcefully remove a non-empty directory and all its contents without prompting.         |
| `rm -r dirname1 dirname2 dirname3`               | Remove multiple directories at once.                                                   |



# A to Z Linux Commands

# Linux Commands Cheat Sheet

## A

| Command   | Description                                                  |
|-----------|--------------------------------------------------------------|
| `&`       | Start a new process in the background.                       |
| `alias`   | Create an alias.                                             |
| `apropos` | Search help manual pages.                                    |
| `apt`     | Search for and install software packages (Debian/Ubuntu).    |
| `apt-get` | Search for and install software packages (Debian/Ubuntu).    |
| `aptitude`| Search for and install software packages (Debian/Ubuntu).    |
| `aspell`  | Spell checker.                                               |
| `at`      | Schedule a command to run once at a specific time.           |
| `awk`     | Find and replace text, database sort/validate/index.         |

## B

| Command      | Description                                                  |
|--------------|--------------------------------------------------------------|
| `basename`   | Strip directory and suffix from filenames.                   |
| `base32`     | Encode/decode data in base32 format.                         |
| `base64`     | Encode/decode data in base64 format.                         |
| `bash`       | GNU Bourne-Again SHell.                                      |
| `bc`         | Arbitrary precision calculator language.                     |
| `bg`         | Send a process to the background.                           |
| `bind`       | Set or display readline key and function bindings.           |
| `bzip2`      | Compress or decompress named file(s).                        |

## C

| Command     | Description                                                  |
|-------------|--------------------------------------------------------------|
| `cal`       | Display a calendar.                                          |
| `cat`       | Concatenate and display the content of files.                |
| `cd`        | Change directory.                                            |
| `chmod`     | Change access permissions.                                   |
| `chown`     | Change file owner and group.                                 |
| `cp`        | Copy one or more files to another location.                  |
| `cron`      | Daemon to execute scheduled commands.                        |
| `crontab`   | Schedule a command to run at a later time.                   |
| `curl`      | Transfer data from or to a server.                           |

## D

| Command      | Description                                                  |
|--------------|--------------------------------------------------------------|
| `date`       | Display or change the date & time.                           |
| `df`         | Display free disk space.                                     |
| `diff`       | Display the differences between two files.                   |
| `dig`        | DNS lookup.                                                  |
| `dir`        | Briefly list directory contents.                             |
| `dirname`    | Convert a full pathname to just a path.                      |
| `dmesg`      | Print kernel & driver messages.                              |
| `du`         | Estimate file space usage.                                   |

## E

| Command      | Description                                                  |
|--------------|--------------------------------------------------------------|
| `echo`       | Display a message on screen.                                 |
| `env`        | Display or modify environment variables.                     |
| `eval`       | Evaluate several commands/arguments.                         |
| `exit`       | Exit the shell.                                              |
| `export`     | Set an environment variable.                                 |

## F

| Command      | Description                                                  |
|--------------|--------------------------------------------------------------|
| `fg`         | Send a job to the foreground.                                |
| `find`       | Search for files meeting specific criteria.                  |
| `free`       | Display memory usage.                                        |
| `fsck`       | File system consistency check and repair.                    |
| `ftp`        | File Transfer Protocol client.                               |
| `function`   | Define function macros.                                      |

## G

| Command       | Description                                                  |
|---------------|--------------------------------------------------------------|
| `gawk`        | Find and replace text within files.                          |
| `getopts`     | Parse positional parameters.                                 |
| `getfacl`     | Get file access control lists.                               |
| `grep`        | Search file(s) for lines that match a given pattern.         |
| `groupadd`    | Add a user security group.                                   |
| `groupdel`    | Delete a group.                                              |
| `groupmod`    | Modify a group.                                              |
| `groups`      | Print group names a user is in.                              |
| `gzip`        | Compress or decompress named file(s).                        |

## H

| Command      | Description                                                  |
|--------------|--------------------------------------------------------------|
| `hash`       | Remember the full pathname of a name argument.               |
| `head`       | Output the first part of file(s).                            |
| `help`       | Display help for a built-in command.                         |
| `history`    | Command history.                                             |
| `hostname`   | Print or set the system name.                                |
| `htop`       | Interactive process viewer.                                  |

## I

| Command      | Description                                                  |
|--------------|--------------------------------------------------------------|
| `iconv`      | Convert the character set of a file.                         |
| `id`         | Print user and group IDs.                                    |
| `if`         | Conditionally perform a command.                             |
| `ifconfig`   | Configure a network interface.                               |
| `install`    | Copy files and set attributes.                               |
| `iostat`     | Report CPU and I/O statistics.                               |
| `ip`         | Routing, devices, and tunnels.                               |

## J

| Command      | Description                                                  |
|--------------|--------------------------------------------------------------|
| `jobs`       | List active jobs.                                            |
| `join`       | Join lines on a common field.                                |

## K

| Command      | Description                                                  |
|--------------|--------------------------------------------------------------|
| `kill`       | Kill a process by specifying its PID.                        |
| `killall`    | Kill processes by name.                                      |

## L

| Command      | Description                                                  |
|--------------|--------------------------------------------------------------|
| `less`       | Display output one screen at a time.                         |
| `ln`         | Create a symbolic link to a file.                            |
| `locate`     | Find files.                                                  |
| `logout`     | Exit a login shell.                                          |
| `lsof`       | List open files.                                             |
| `ls`         | List information about files.                                |

## M

| Command      | Description                                                  |
|--------------|--------------------------------------------------------------|
| `make`       | Recompile a group of programs.                               |
| `man`        | Display the help manual.                                     |
| `mkdir`      | Create new directories.                                      |
| `mount`      | Mount a file system.                                         |
| `mv`         | Move or rename files or directories.                         |

## N

| Command      | Description                                                  |
|--------------|--------------------------------------------------------------|
| `nc`         | Netcat - read and write data across networks.                |
| `netstat`    | Display networking connections and stats.                    |
| `nice`       | Set the priority of a command or job.                        |
| `nohup`      | Run a command immune to hangups.                             |
| `nslookup`   | Query Internet name servers interactively.                   |

## O

| Command      | Description                                                  |
|--------------|--------------------------------------------------------------|
| `open`       | Open a file in its default application.                      |
| `op`         | Operator access.                                             |

## P

| Command      | Description                                                  |
|--------------|--------------------------------------------------------------|
| `passwd`     | Modify a user password.                                      |
| `paste`      | Merge lines of files.                                        |
| `ping`       | Test a network connection.                                   |
| `pkill`      | Kill processes by name.                                      |
| `printf`     | Format and print data.                                       |
| `ps`         | Display process status.                                      |
| `pwd`        | Print working directory.                                     |

## Q

| Command      | Description                                                  |
|--------------|--------------------------------------------------------------|
| `quota`      | Display disk usage and limits.                               |
| `quotacheck` | Scan a file system for disk usage.                           |

## R

| Command      | Description                                                  |
|--------------|--------------------------------------------------------------|
| `reboot`     | Reboot the system.                                           |
| `rename`     | Rename files.                                                |
| `rm`         | Remove files.                                                |
| `rmdir`      | Remove directories.                                          |
| `rsync`      | Remote file copy (synchronize file trees).                   |

## S

| Command       | Description                                                  |
|---------------|--------------------------------------------------------------|
| `screen`      | Multiplex terminal, run remote shells via ssh.               |
| `scp`         | Secure copy (remote file copy).                              |
| `sdiff`       | Merge two files interactively.                               |
| `sed`         | Stream Editor.                                               |
| `select`      | Accept user choices via keyboard input.                      |
| `seq`         | Print numeric sequences.                                     |
| `set`         | Manipulate shell variables and functions.                    |
| `setfacl`     | Set file access control lists.                               |
| `sftp`        | Secure File Transfer Program.                                |
| `shift`       | Shift positional parameters.                                 |
| `shopt`       | Shell options.                                               |
| `shuf`        | Generate random permutations.                                |
| `shutdown`    | Shutdown or restart Linux.                                   |
| `sleep`       | Delay for a specified time.                                  |
| `slocate`     | Find files (faster than `locate` on large databases).        |
| `sort`        | Sort text files.                                             |
| `source`      | Run commands from a file (same as `.`).                       |
| `split`       | Split a file into fixed-size pieces.                         |
| `ss`          | Socket statistics.                                            |
| `ssh`         | Secure Shell client (remote login program).                   |
| `stat`        | Display file or file system status.                          |
| `strace`      | Trace system calls and signals.                              |
| `su`          | Substitute user identity.                                    |
| `sudo`        | Execute a command as another user.                           |
| `sum`         | Print a checksum for a file.                                 |
| `suspend`     | Suspend execution of this shell.                             |
| `sync`        | Synchronize data on disk with memory.                        |


## T

| Command       | Description                                                  |
|---------------|--------------------------------------------------------------|
| `tail`        | Output the last part of a file.                              |
| `tar`         | Store, list, or extract files in an archive.                 |
| `tee`         | Redirect output to multiple files.                           |
| `test`        | Evaluate a conditional expression.                           |
| `time`        | Measure program running time.                                |
| `timeout`     | Run a command with a time limit.                             |
| `times`       | Display user and system times.                               |
| `tmux`        | Terminal multiplexer.                                        |
| `touch`       | Change file timestamps.                                      |
| `top`         | List processes running on the system.                        |
| `traceroute`  | Trace route to a host.                                       |
| `trap`        | Execute a command when the shell receives a signal.          |
| `tr`          | Translate, squeeze, and/or delete characters.                |
| `true`        | Do nothing successfully.                                     |
| `tsort`       | Perform topological sorting.                                 |
| `tty`         | Print the filename of the terminal connected to stdin.       |
| `type`        | Describe a command.                                          |

## U

| Command       | Description                                                  |
|---------------|--------------------------------------------------------------|
| `ulimit`      | Limit user resources.                                        |
| `umask`       | Set user file creation mask.                                 |
| `umount`      | Unmount a device.                                            |
| `unalias`     | Remove an alias.                                             |
| `uname`       | Print system information.                                    |
| `uniq`        | Filter unique lines from sorted files.                       |
| `units`       | Convert units from one scale to another.                     |
| `unset`       | Remove a variable or function.                               |
| `until`       | Execute commands until a condition is true.                  |
| `uptime`      | Show system uptime.                                          |
| `useradd`     | Create a new user account.                                   |
| `userdel`     | Delete a user account.                                       |
| `usermod`     | Modify a user account.                                       |
| `users`       | List users currently logged in.                              |

## V

| Command       | Description                                                  |
|---------------|--------------------------------------------------------------|
| `vi`          | Text editor.                                                 |
| `vmstat`      | Report virtual memory statistics.                            |

## W

| Command       | Description                                                  |
|---------------|--------------------------------------------------------------|
| `w`           | Show who is logged on and what they are doing.               |
| `wait`        | Wait for a process to complete.                              |
| `watch`       | Execute/display a program periodically.                      |
| `wc`          | Print byte, word, and line counts.                           |
| `whereis`     | Locate the binary, source, and manual page files for a command. |
| `which`       | Locate a command's executable file in the user's $PATH.      |
| `who`         | Print all usernames currently logged in.                     |
| `whoami`      | Print the current user ID and name.                          |
| `wget`        | Retrieve web pages or files via HTTP, HTTPS, or FTP.         |
| `write`       | Send a message to another user.                              |

## X

| Command       | Description                                                  |
|---------------|--------------------------------------------------------------|
| `xargs`       | Execute a utility passing constructed argument list(s).      |
| `xdg-open`    | Open a file or URL in the user's preferred application.       |
| `xxd`         | Make a hexdump or do the reverse.                            |
| `xz`          | Compress or decompress `.xz` and `.lzma` files.              |

## Y

| Command       | Description                                                  |
|---------------|--------------------------------------------------------------|
| `yes`         | Print a string repeatedly until interrupted.                 |

## Z

| Command       | Description                                                  |
|---------------|--------------------------------------------------------------|
| `zip`         | Package and compress (archive) files.                        |
| `zcat`        | View the contents of a compressed file.                      |
| `zgrep`       | Search inside compressed files.                              |
| `zless`       | View compressed files one screen at a time.                  |
| `zmore`       | Browse through compressed files.                             |
| `znew`        | Recompress `.z` files to `.gz` format.                       |

# Another Cheatsheet

![image](https://github.com/user-attachments/assets/70b8faee-6f25-4405-8b47-ea082934b444)




