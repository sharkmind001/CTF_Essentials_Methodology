### Linux File Hierarchy Structure (FHS)

The Linux File Hierarchy Structure (FHS) defines the directory structure and contents of the Linux filesystem. Below is a table summarizing the key directories and their specifications.

| **Directory**  | **Full Name**           | **Specification**                                                                                           |
|----------------|-------------------------|-------------------------------------------------------------------------------------------------------------|
| `/`            | Root                    | The root directory, the top-level directory in the filesystem. All other directories are under this directory. |
| `/bin`         | Binaries                | Contains essential system binaries and commands required by all users.                                      |
| `/boot`        | Boot system             | Contains files necessary to boot the system, including the kernel, boot loader, and initial RAM disk.         |
| `/dev`         | Devices                 | Contains device files that represent hardware devices connected to the system.                              |
| `/etc`         | Configuration Files     | Contains configuration files for the system and applications.                                               |
| `/home`        | All user data           | Contains home directories for users.                                                                         |
| `/lib`         | Libraries               | Contains system libraries needed by programs in `/bin` and `/sbin`.                                         |
| `/mnt`         | Mount                   | Used for temporarily mounting external file systems.                                                        |
| `/media`       | Removable devices       | Used for mounting removable media devices such as USB drives and CD/DVDs.                                    |
| `/opt`         | Optional                | Used for installing optional software packages.                                                              |
| `/proc`        | Process                 | A virtual file system that contains information about system processes and resources.                       |
| `/root`        | Admin folder            | The home directory for the root user.                                                                        |
| `/sbin`        | System binaries         | Contains system binaries and commands for system administration.                                           |
| `/tmp`         | Temporary               | Used for storing temporary files.                                                                            |
| `/usr`         | User                    | Contains most of the system software, including user utilities, applications, and libraries.                |
| `/var`         | Variable                | Contains variable data, such as log files, spool directories, and other temporary files.                    |
| `/srv`         | Served by System        | Contains data for services provided by the system, such as website files or FTP data.                       |
| `/sys`         | System                  | A virtual file system that contains information about the system's hardware devices and drivers.            |
| `/run`         | Running                 | Contains runtime data, such as process IDs and system status information.                                   |

### Description of Key Directories

1. **/ (Root)**  
   - Every file and directory starts from the root directory.  
   - Only the root user has write privileges under this directory.  
   - `/root` is the root user’s home directory, which is not the same as `/`.

2. **/bin (User Binaries)**  
   - Contains binary executables.  
   - Common Linux commands are located here.  
   - Examples: `ps`, `ls`, `ping`, `grep`, `cp`.

3. **/sbin (System Binaries)**  
   - Contains system binaries, used by system administrators for maintenance.  
   - Examples: `iptables`, `reboot`, `fdisk`, `ifconfig`, `swapon`.

4. **/etc (Configuration Files)**  
   - Contains configuration files for all programs and system startup/shutdown scripts.  
   - Examples: `/etc/resolv.conf`, `/etc/logrotate.conf`.

5. **/dev (Device Files)**  
   - Contains device files representing hardware devices.  
   - Examples: `/dev/tty1`, `/dev/usbmon0`.

6. **/proc (Process Information)**  
   - A pseudo filesystem with information about running processes.  
   - Examples: `/proc/{pid}`, `/proc/uptime`.

7. **/var (Variable Files)**  
   - Contains files that are expected to grow, such as system logs, databases, and email files.  
   - Examples: `/var/log`, `/var/mail`, `/var/spool`, `/var/tmp`.

8. **/tmp (Temporary Files)**  
   - Stores temporary files created by the system and users.  
   - Files in this directory are deleted after reboot.

9. **/usr (User Programs)**  
   - Contains binaries, libraries, documentation, and source code for second-level programs.  
   - Example directories: `/usr/bin`, `/usr/sbin`, `/usr/lib`, `/usr/local`.

10. **/home (Home Directories)**  
    - Contains personal directories for users.  
    - Example: `/home/john`, `/home/nikita`.

11. **/boot (Boot Loader Files)**  
    - Contains files necessary for booting the system, including the kernel and boot loader files.  
    - Examples: `vmlinuz`, `initrd.img`.

12. **/lib (System Libraries)**  
    - Contains libraries that support binaries located in `/bin` and `/sbin`.  
    - Examples: `ld-2.11.1.so`, `libncurses.so.5.7`.

13. **/opt (Optional Add-on Applications)**  
    - Contains add-on applications from third-party vendors.  
    - Example: `/opt/apache2`.

14. **/mnt (Mount Directory)**  
    - A temporary mount directory where system administrators mount filesystems.

15. **/media (Removable Media Devices)**  
    - A temporary mount directory for removable devices.  
    - Examples: `/media/cdrom`, `/media/usb`.

16. **/srv (Service Data)**  
    - Contains data related to services provided by the system.  
    - Example: `/srv/www` for web server data.

