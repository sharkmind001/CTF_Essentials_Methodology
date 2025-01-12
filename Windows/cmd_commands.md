# CMD Commands

| **Command/Function**                                           | **Description**                                                                                             |
|---------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------|
| `ctrl + r`                                                     | Type command                                                                                                 |
| `ctrl + shift + enter`                                         | Open cmd with administrator privileges                                                                      |
| `dir /?`                                                       | Help for any command                                                                                         |
| `tasklist /?`                                                  | Help for any command                                                                                         |
| `md amit`                                                      | Make folder                                                                                                  |
| `mkdir amit`                                                   | Make directory                                                                                                |
| `rmdir amit`                                                   | Delete directory                                                                                              |
| `copy cmdnotes.txt "test"`                                     | Copy file                                                                                                     |
| `copy *.txt "test"`                                            | Copy multiple files                                                                                          |
| `del cmdnotes.txt`                                             | Delete file                                                                                                   |
| `move cmdnotes.txt "test"`                                     | Move file                                                                                                     |
| `ren cmdnotes.txt cmd.txt`                                     | Rename file                                                                                                   |
| `rem amit sumit`                                               | Rename folder                                                                                                 |

> ## Findstr

| **Command/Function**                                                              | **Description**                                                                                          |
|-----------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------|
| `systeminfo \| findstr /C:"processor"`                                             | Find a string                                                                                             |
| `systeminfo \| findstr "processor"`                                                | Find a string (default behavior)                                                                          |
| `findstr /bi /F:"processor"`                                                      | Find a file                                                                                               |
| `findstr /bi /D:"processor"`                                                      | Find a directory                                                                                          |
| `systeminfo \| findstr /b "processo"`                                              | Automatically complete remaining word matching the given word                                              |
| `systeminfo \| findstr /i "ProCessor"`                                             | Bypass case sensitivity                                                                                    |
| `systeminfo \| findstr /bi "ProCess"`                                             | Bypass case sensitivity and matching word                                                                 |
| `findstr "computer help" myfile.txt`                                               | Find in a specified text file                                                                              |
| `findstr /s "computer help" *.txt`                                                 | Find in current and all subdirectories                                                                    |
| `findstr /s /x "computer help" *.txt`                                              | Find exact match in current and all subdirectories                                                       |
| `findstr /x /c:"computer help" *.*`                                                | Find exact match across all files                                                                          |
| `findstr /s "KB.." *.txt`                                                         | Find any word matching the pattern in `.txt` files                                                       |


> ##  File Operations

| **Command**                                                      | **Description**                                                                  |
|------------------------------------------------------------------|----------------------------------------------------------------------------------|
| `type nul> file1.txt`                                             | Create an empty file                                                            |
| `more file1.txt`                                                 | To read a text file in cmd                                                       |
| `type nul> file2.ppt`                                             | Create a PowerPoint file                                                         |
| `copy con context.txt`                                            | Create a text file with content (type content and press ^Z)                       |
| `C:\Users\superuser>copy con amit.txt this is cmd (press ^Z)`      | To create a file and write data                                                  |
| `echo it is cmd> file1.txt`                                       | Create a text file using echo                                                    |
| `cipher /e`                                                      | Encrypt all files in the current folder                                          |
| `cipher /d`                                                      | Decrypt files                                                                    |
| `cipher /e amit.txt`                                             | Encrypt the file `amit.txt`                                                      |
| `attrib +h +r +s amit.txt`                                        | Hide a file                                                                      |
| `attrib -h -r -s amit.txt`                                        | Unhide a file                                                                    |

> ##  Process Management

| **Command**                                                      | **Description**                                                                  |
|------------------------------------------------------------------|----------------------------------------------------------------------------------|
| `tasklist`                                                       | Show running processes                                                           |
| `taskkill /pid 9716`                                             | Kill a process by its PID                                                        |
| `net start`                                                      | Show running services                                                            |
| `net stop "themes"`                                              | Stop a service                                                                   |
| `net start "themes"`                                             | Start a service                                                                  |
| `net stop "windows audio"`                                        | Stop the audio service                                                           |

> ##  Driver Management

| **Command**                                                      | **Description**                                                                  |
|------------------------------------------------------------------|----------------------------------------------------------------------------------|
| `driverquery`                                                    | Show all drivers                                                                 |
| `windows + r and type`                                           | Open Firewall settings (`firewall.cpl`)                                          |
| `netsh advfirewall set all state off`                            | Turn off the firewall using netsh                                                |
| `netsh advfirewall set all state on`                             | Turn on the firewall using netsh                                                 |

> ##  WMIC (Windows Management Instrumentation)

| **Command**                                                      | **Description**                                                                  |
|------------------------------------------------------------------|----------------------------------------------------------------------------------|
| `wmic cpu`                                                       | Show information about the processor                                             |
| `wmic bios get serialnumber`                                     | Show BIOS serial number                                                          |
| `wmic computersystem get totalphysicalmemory`                    | Show total physical memory (in bytes)                                            |
| `wmic nic get macaddress`                                        | Show the MAC address of the network interface card                               |
| `wmic partition get name, size, type`                            | Show partition information                                                       |
| `wmic process list brief`                                         | Show a brief list of running processes                                            |
| `wmic process where name="notepad.exe" call terminate`           | Kill the Notepad process by name                                                 |
| `wmic product get name, version`                                  | Show installed applications                                                      |
| `wmic service get name, startname`                                | Show name and account of all services                                             |
| `wmic service where started=true get name, startname`             | Show only the services that are currently running                                 |


> ##  User and Groups

| **Command**                                                      | **Description**                                                                  |
|------------------------------------------------------------------|----------------------------------------------------------------------------------|
| `net user`                                                       | Show all users                                                                  |
| `net user <username> /add`                                        | Add a new user without a password                                               |
| `net user <user> <pass> /add`                                     | Create a new user with a password                                                |
| `net user amit amit@123 /add`                                     | Create a new user with specified password                                        |
| `net user amit /del`                                              | Delete a user                                                                   |
| `net user administrator /active:yes`                              | Enable a user                                                                   |
| `net user administrator /active:no`                               | Disable a user                                                                  |
| `net user amit *`                                                 | Reset the password of any user                                                  |

> ##  System Information

| **Command**                                                      | **Description**                                                                  |
|------------------------------------------------------------------|----------------------------------------------------------------------------------|
| `vol C:`                                                         | Get serial number and volume information                                        |
| `winver`                                                         | Show Windows version                                                            |
| `chkdsk`                                                         | Check the file system, free space, and disk health                              |
| `getmac`                                                         | Show MAC address                                                                |
| `systeminfo`                                                     | Get system information                                                          |
| `diskpart`                                                       | Enter into diskpart shell                                                       |
| `list disk`                                                      | Show all disks                                                                  |
| `select disk 0`                                                  | Select a specific disk (e.g., disk 0)                                            |
| `detail disk`                                                    | Show detailed information about the selected disk                               |
| `exit`                                                           | Exit from diskpart shell                                                        |

> ##  Disk Formatting

| **Command**                                                      | **Description**                                                                  |
|------------------------------------------------------------------|----------------------------------------------------------------------------------|
| `diskpart`                                                       | Open diskpart shell                                                             |
| `list disk`                                                      | Show all disks                                                                  |
| `select disk 1`                                                  | Select disk 1                                                                   |
| `clean`                                                          | Clean the disk (delete all data)                                                |
| `create partition primary`                                       | Create a primary partition                                                      |
| `select partition 1`                                              | Select partition 1                                                              |
| `format fs=ntfs quick`                                            | Format the partition to NTFS file system (quick format)                         |
| `format fs=fat32 quick`                                           | Format the partition to FAT32 file system (quick format)                        |
| `active`                                                         | Mark the partition as active for booting                                        |
| `assign`                                                         | Assign a letter to the partition (make it accessible)                           |
| `exit`                                                           | Exit diskpart                                                                 |
| `label E: amit`                                                  | Change the label of the drive to `amit`                                          |

> ##  Bootable USB

| **Command**                                                      | **Description**                                                                  |
|------------------------------------------------------------------|----------------------------------------------------------------------------------|
| Download OS ISO file                                              | Download the operating system ISO file                                          |
| Right-click on ISO file, click mount                               | Mount the ISO file to access its contents                                        |
| Select all files and paste in pendrive                           | Copy the ISO contents to the USB drive to make it bootable                      |

> ##  Netsh (Network Shell)

| **Command**                                                      | **Description**                                                                  |
|------------------------------------------------------------------|----------------------------------------------------------------------------------|
| `win+r = ncpa.cpl`                                               | Show the current Wi-Fi password                                                 |
| `netsh wlan show profile redmi key=clear`                        | Show the password of a saved Wi-Fi profile                                      |
| `netsh wlan delete profile name=redmi`                            | Forget the saved Wi-Fi profile                                                  |
| `netsh wlan set hostednetwork mode=allow ssid=mywifi key=amit@123` | Create a Wi-Fi hotspot with a specified SSID and password                        |
| `netsh wlan start hostednetwork`                                 | Start the Wi-Fi hotspot                                                         |
| `netsh wlan stop hostednetwork`                                  | Stop the Wi-Fi hotspot                                                          |
| `netsh wlan show profiles`                                       | Show all saved Wi-Fi profiles                                                   |
| `netsh wlan show all`                                            | Show all information about surrounding Wi-Fi networks                            |

> ##  Networking

| **Command**                                                      | **Description**                                                                  |
|------------------------------------------------------------------|----------------------------------------------------------------------------------|
| `ping www.google.com`                                             | Check network connection to a website                                           |
| `tracert www.google.com`                                          | Show the route taken by packets to reach a website                               |
| `netstat -e`                                                     | Show network statistics                                                         |
| `nslookup`                                                       | Show DNS records for a domain                                                   |

> ##  Color

| **Command**                                                      | **Description**                                                                  |
|------------------------------------------------------------------|----------------------------------------------------------------------------------|
| `color ?`                                                        | Show all available color options for the terminal                               |
| `color 0c`                                                       | Change text color to red (or any other color)                                   |
| `color 0a`                                                       | Change background to green and text color to black                              |
| `color 1a`                                                       | Change background to green and text color to blue                               |

> ##  Shutdown

| **Command**                                                      | **Description**                                                                  |
|------------------------------------------------------------------|----------------------------------------------------------------------------------|
| `title abc`                                                      | Change the title of the command prompt window                                   |
| `mode 250`                                                       | Change the terminal window size                                                 |
| `doskey/history`                                                 | Show the command history in the command prompt                                  |
| `shutdown -s -t 00`                                              | Shutdown the system immediately                                                 |
| `shutdown -r -t 00`                                              | Restart the system immediately                                                  |


> ## Bootable usb:

    1) download os iso file.
    2) Right click on iso file click mount
    3) Select all files and paste in pendrive

> ## Netsh(network shell):


| **Command**                                                        | **Description**                                                                |
|--------------------------------------------------------------------|--------------------------------------------------------------------------------|
| `win+r = ncpa.cpl`                                                 | Show current Wi-Fi password                                                   |
| `netsh wlan show profile redmi key=clear`                          | Show password of a saved Wi-Fi profile                                         |
| `netsh wlan delete profile name=redmi`                              | Forget the saved Wi-Fi profile                                                 |
| `netsh wlan set hostednetwork mode=allow ssid=mywifi key=amit@123` | Create a Wi-Fi hotspot with the specified SSID and password                    |
| `netsh wlan start hostednetwork`                                   | Start the Wi-Fi hotspot                                                       |
| `netsh wlan stop hostednetwork`                                    | Stop the Wi-Fi hotspot                                                        |
| `netsh wlan show profiles`                                         | Show all saved Wi-Fi profiles                                                  |
| `netsh wlan show all`                                              | Show all information about surrounding Wi-Fi networks                          |


> ## Batch script:

Save with .bat or .exe extension of the following script.
```
@echo off 
color 0a          
echo welcome to batch scripting.
pause 
```
• echo off is used to hide directories(during execurtion) path between every command and @ only show command execution without show any directory.

• pause is used to hold screen during execution.

> ## Comment:
```
@echo off      
color 0a          
echo welcome to batch scripting.
rem this is a comment
pause
```
• echo off, @echo off are used to reduce unwanted output)
• rem used to comment

> ## Declare a variable:
```
@echo off
set /a var1=12         
set var2=Amit		
echo The student name is %var2% and his age is %var1% 
pause
```
• "/a" for int variable
• Without "/a" used to char variable
• %var% used to print variables

> ## User input:
```
@echo off
set /p var3=enter your name        
set /p var4=enter your age
echo The student name is %var3% and age is %var4%
pause
```
• "/p" for prompt

> ## If-Else statement:
```
@echo off
set /p var1=
if %var1% == 18 (echo you can vote) else (echo you can't vote)
pause
```
> ## Arrays:
```
set n1[0]=1      
set n1[1]=2
set n1[2]=3
echo %n1[1]% and %n1[2]%
```
• [0] it is index
• %n1[2]% used to print arrays.

> ## Function:












