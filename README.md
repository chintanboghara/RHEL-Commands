## File and Directory Management

- `ls` - List files and directories
- `cd` - Change directory
- `pwd` - Print current working directory
- `mkdir` - Create a new directory
- `rm` - Remove files and directories
- `cp` - Copy files and directories
- `mv` - Move or rename files and directories
- `touch` - Create an empty file or update file timestamps
- `cat` - Display the contents of a file
- `head` - Display the first few lines of a file
- `tail` - Display the last few lines of a file
- `ln` - Create links between files
- `find` - Search for files and directories
- `locate` - Find files by name (requires `mlocate` package)
- `updatedb` - Update the file database used by `locate`

## File Permission Commands

- `chmod` - Change file permissions
- `chown` - Change file ownership
- `chgrp` - Change group ownership
- `umask` - Set default file permissions

## File Compression and Archiving Commands

- `tar` - Create or extract archive files
- `gzip` - Compress files
- `gunzip` - Decompress files compressed with `gzip`
- `zip` - Create compressed zip archives
- `unzip` - Extract files from a zip archive

## Process Management Commands

- `ps` - Display running processes
- `top` - Monitor system processes in real-time
- `kill` - Terminate a process
- `pkill` - Terminate processes based on their name
- `pgrep` - List processes based on their name
- `nohup` - Run a command immune to hangups

## System Information Commands

- `uname` - Print system information
- `whoami` - Display current username
- `free` - Display memory usage information
- `uptime` - Show system uptime
- `lscpu` - Display CPU information
- `lspci` - List PCI devices
- `lsusb` - List USB devices
- `lsof` - List open files and processes
- `lshw` - Display detailed hardware configuration (may require installation)
- `sar` - Collect and report system activity information (part of `sysstat` package)
- `date` - Display or set the system date and time
- `cal` - Display a calendar

## Networking Commands

- `ip addr show` - Display network interface information (preferred over `ifconfig`)
- `ip link set dev eth0 up` - Bring up a network interface
- `ip route` - Display or manipulate the IP routing table (preferred over `route`)
- `ping` - Send ICMP echo requests to a host
- `ss` - Display network socket information (preferred over `netstat`)
- `ssh` - Securely connect to a remote server
- `scp` - Securely copy files between hosts
- `wget` - Download files from the web
- `curl` - Transfer data to or from a server
- `rsync` - Synchronize files and directories between systems
- `iftop` - Display network bandwidth usage (may require installation)
- `nc` - Netcat utility for network connections
- `iptables` - Administer IPv4 packet filtering and NAT (alternative: `firewalld` on RHEL)
- `ssh-keygen` - Generate SSH key pairs

**Note:** `ipconfig` is a Windows command and not applicable to RHEL. `ifconfig`, `netstat`, and `route` are deprecated in favor of `ip` and `ss` commands on modern RHEL systems.

## IO Redirection

- `cmd < file` - Input of `cmd` is taken from `file`
- `cmd > file` - Standard output of `cmd` is redirected to `file`
- `cmd 2> file` - Error output of `cmd` is redirected to `file`
- `cmd &> file` - All output of `cmd` is redirected to `file`
- `cmd >> file` - Append the standard output of `cmd` to `file`
- `tee` - Redirect output to multiple files or processes

## Environment Variable Commands

- `export VARIABLE_NAME=value` - Set an environment variable
- `echo $VARIABLE_NAME` - Display an environment variable's value
- `env` - List all environment variables
- `unset VARIABLE_NAME` - Remove an environment variable

## User Management Commands

- `who` - Show who is currently logged in
- `useradd username` - Create a new user account (preferred over `adduser` on RHEL)
- `finger` - Display information about users
- `usermod -aG groupname username` - Add a user to a group
- `last` - Show recent login history
- `userdel -r username` - Delete a user account and its files
- `passwd -l username` - Lock a user account
- `su - username` - Switch to another user account

**Note:** `adduser` is more common on Debian-based systems; RHEL typically uses `useradd`. `deluser` is not a standard RHEL command; use `groupmod` or `usermod` for group management.

## Shell Commands

- `alias` - Create an alias for a command
- `source` - Execute commands from a file in the current shell
- `history` - Display the command history

## Scheduling Commands

- `crontab` - Schedule commands or scripts to run periodically

## Text Processing Commands

- `grep` - Search for patterns in text
- `awk` - Text processing tool for data extraction and manipulation
- `sed` - Stream editor for text manipulation
- `diff` - Compare files line by line
- `sort` - Sort lines of text files
- `cut` - Extract sections from lines of files
- `wc` - Count lines, words, and characters in a file

## General Commands

- `man` - Display the manual pages for a command
- `which` - Display the location of a command
- `sudo` - Run a command with administrative privileges

## System Control Commands

- `shutdown` - Shut down or reboot the system
- `reboot` - Reboot the system
- `halt` - Halt the system
- `systemctl restart service_name` - Restart a service (RHEL uses `systemd`)
- `systemctl status service_name` - Check the status of a service
- `systemctl enable service_name` - Enable a service to start on boot

## Bash Shortcuts

- `Ctrl + A` - Move to the beginning of the line
- `Ctrl + E` - Move to the end of the line
- `Ctrl + B` - Move back one character
- `Ctrl + F` - Move forward one character
- `Alt + B` - Move back one word
- `Alt + F` - Move forward one word
- `Ctrl + U` - Cut from cursor to beginning of line
- `Ctrl + K` - Cut from cursor to end of line
- `Ctrl + W` - Cut the word before the cursor
- `Ctrl + Y` - Paste the last cut text
- `Ctrl + L` - Clear the screen
- `Ctrl + R` - Search command history
- `Ctrl + G` - Escape from history search mode
- `Ctrl + P` - Go to previous command in history
- `Ctrl + N` - Go to next command in history
- `Ctrl + C` - Terminate the current command

## Nano Shortcuts

- `Ctrl + O` - Save the file
- `Ctrl + X` - Exit Nano
- `Ctrl + R` - Read a file into the current buffer
- `Ctrl + J` - Justify the current paragraph
- `Ctrl + Y` - Scroll up one page
- `Ctrl + V` - Scroll down one page
- `Alt + \` - Go to a specific line number
- `Alt + ,` - Go to the beginning of the current line
- `Alt + .` - Go to the end of the current line
- `Ctrl + K` - Cut from cursor to end of line
- `Ctrl + U` - Uncut/restore the last cut text
- `Ctrl + 6` - Mark a block of text
- `Ctrl + W` - Search for a string
- `Alt + W` - Search and replace a string
- `Alt + R` - Repeat the last search

## VI Shortcuts

- `cw` - Change the current word
- `dd` - Delete the current line
- `x` - Delete the character under the cursor
- `R` - Enter replace mode
- `o` - Insert a new line below and enter insert mode
- `u` - Undo the last change
- `s` - Substitute the character under the cursor
- `dw` - Delete from cursor to beginning of next word
- `D` - Delete from cursor to end of line
- `4dw` - Delete the next four words
- `A` - Append at the end of the line
- `S` - Delete the current line and enter insert mode
- `r` - Replace the character under the cursor
- `i` - Insert before the cursor
- `3dd` - Delete three lines
- `ESC` - Exit insert mode
- `U` - Restore the current line
- `~` - Switch case of the character
- `a` - Append after the cursor
- `C` - Change from cursor to end of line

## Vim Shortcuts

- `i` - Enter insert mode
- `x` - Delete the character under the cursor
- `dd` - Delete the current line
- `yy` - Copy the current line
- `p` - Paste below the current line
- `u` - Undo the last change
- `Ctrl + R` - Redo the last undo
- `:w` - Save the file
- `:q` - Quit Vim
- `:wq` - Save and quit
- `:q!` - Quit without saving
- `:set nu` - Display line numbers
- `v` - Enter visual mode
- `y` - Copy the selected text
- `d` - Delete the selected text
- `p` - Paste the copied or deleted text
- `:s/old/new/g` - Replace all occurrences of 'old' with 'new'

## Package Management Commands

- `yum update` - Update package list and upgrade installed packages (RHEL 7 and earlier)
- `yum install package_name` - Install a package (RHEL 7 and earlier)
- `dnf update` - Update package list and upgrade installed packages (RHEL 8 and later)
- `dnf install package_name` - Install a package (RHEL 8 and later)
- `dnf search pattern` - Search for packages (RHEL 8 and later)
- `dnf list installed` - List installed packages (RHEL 8 and later)
- `rpm -i package.rpm` - Install an RPM package file

**Note:** `apt`, `dpkg`, and `pacman` commands are not applicable to RHEL; they are used on Debian-based and Arch Linux systems, respectively.

## Disk Space Usage & Monitoring

- `df -h` - Show disk space usage in human-readable format
- `du -sh /var/log` - Show size of a specific directory
- `du -h --max-depth=1` - Show sizes of subdirectories (1 level deep)
- `lsblk` - Display information about block devices (partitions & disks)
- `blkid` - Show UUID and filesystem type of partitions
- `findmnt` - Display mounted filesystems
- `mount | column -t` - List mounted files in a readable table format

## Partition & Filesystem Management

- `fdisk -l` - Show partition table of all disks
- `parted -l` - Display partition details using GNU Parted
- `mkfs.ext4 /dev/sdb1` - Format a partition with ext4 filesystem
- `mkfs.xfs /dev/sdb1` - Format a partition with XFS filesystem (common on RHEL)
- `e2fsck -f /dev/sdb1` - Check and repair an ext4 filesystem
- `xfs_repair /dev/sdb1` - Repair an XFS filesystem
- `tune2fs -m 5 /dev/sdb1` - Set reserved space on ext4 filesystem (5% in this case)

## Mounting & Unmounting Filesystems

- `mount /dev/sdb1 /mnt` - Mount a partition to `/mnt`
- `umount /mnt` - Unmount a filesystem from `/mnt`
- `mount -o remount,rw /` - Remount root filesystem as read-write
- `mount -t nfs 192.168.1.100:/share /mnt` - Mount an NFS share
- `mount -o loop file.iso /mnt` - Mount an ISO file as a virtual disk

## Disk Performance & Health Monitoring

- `iotop` - Show real-time disk I/O usage by processes (may require installation)
- `iostat -x 1` - Show detailed disk usage statistics (part of `sysstat` package)
- `smartctl -H /dev/sda` - Check SMART health status of a disk (part of `smartmontools`)
- `smartctl -a /dev/sda` - Display full SMART diagnostics
- `badblocks -sv /dev/sdb` - Scan for bad sectors on a disk

## Managing Disk Quotas

- `quota -u username` - Show disk quota for a user
- `edquota -u username` - Edit disk quota for a user
- `repquota -a` - Show quota report for all users
- `setquota -u username 500M 1G 0 0 /dev/sda1` - Set quota (500MB soft, 1GB hard)

## LVM (Logical Volume Management)

- `pvcreate /dev/sdb` - Initialize a physical volume for LVM
- `vgcreate vg /dev/sdb` - Create a volume group from a physical volume
- `lvcreate -L 10G -n my_lv my_vg` - Create a 10GB logical volume
- `lvextend -L +5G /dev/my_vg/my_lv` - Extend a logical volume by 5GB
- `resize2fs /dev/my_vg/my_lv` - Resize ext4 filesystem after extending LVM

## Swap Space Management

- `swapon -s` - Show active swap partitions and files
- `free -m` - Display system memory usage including swap
- `mkswap /dev/sdb2` - Format a partition as swap
- `swapon /dev/sdb2` - Enable swap partition
- `swapoff /dev/sdb2` - Disable swap partition
- `fallocate -l 2G /swapfile` - Create a 2GB swap file
- `mkswap /swapfile` - Format swap file
- `swapon /swapfile` - Enable swap file

## Secure Disk Erasing

- `shred -n 3 -z /dev/sdb` - Securely erase a disk by overwriting it 3 times
- `dd if=/dev/zero of=/dev/sdb bs=1M status=progress` - Wipe a disk by filling it with zeroes
- `wipe -rf /dev/sdb` - Securely wipe a disk (requires `wipe` utility, may need installation)

## RHEL Specific Commands

- `subscription-manager register` - Register the system with Red Hat Subscription Management
- `subscription-manager attach --auto` - Attach a subscription to the system
- `firewall-cmd --list-all` - List all firewall rules (uses `firewalld`, RHEL's default firewall)
- `firewall-cmd --add-service=http` - Allow HTTP traffic through the firewall
- `semanage fcontext -a -t httpd_sys_content_t "/my/web(/.*)?"` - Set SELinux file context
- `restorecon -Rv /my/web` - Restore SELinux file contexts
- `getenforce` - Get the current SELinux mode
- `setenforce 0` - Set SELinux to permissive mode
