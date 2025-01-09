## Basic Commands

### System Information
- **Check RHEL version**:  
  `cat /etc/redhat-release`
- **Check kernel version**:  
  `uname -r`
- **View system uptime**:  
  `uptime`
- **Check CPU information**:  
  `lscpu`
- **Check memory usage**:  
  `free -h`
- **Check disk usage**:  
  `df -h`
- **Check mounted filesystems**:  
  `mount | column -t`

### Package Management
- **Install a package**:  
  `sudo yum install <package-name>`
- **Remove a package**:  
  `sudo yum remove <package-name>`
- **Update all packages**:  
  `sudo yum update`
- **Search for a package**:  
  `sudo yum search <package-name>`
- **List installed packages**:  
  `rpm -qa`
- **Check package details**:  
  `rpm -qi <package-name>`

### File and Directory Operations
- **List files**:  
  `ls -l`
- **Create a directory**:  
  `mkdir <directory-name>`
- **Remove a directory**:  
  `rmdir <directory-name>` (empty)  
  `rm -r <directory-name>` (non-empty)
- **Copy a file/directory**:  
  `cp <source> <destination>`
- **Move/rename a file/directory**:  
  `mv <source> <destination>`
- **Delete a file**:  
  `rm <file-name>`
- **View file content**:  
  `cat <file-name>`
- **Edit a file**:  
  `vi <file-name>` or `nano <file-name>`
- **Find files**:  
  `find /path/to/search -name <file-name>`

### Networking
- **Check IP address**:  
  `ip addr show` or `ifconfig`
- **Test connectivity**:  
  `ping <hostname-or-ip>`
- **Check open ports**:  
  `netstat -tuln`
- **Restart network service**:  
  `sudo systemctl restart network`

### Process Management
- **List running processes**:  
  `ps aux`
- **Kill a process**:  
  `kill <PID>`  
  `kill -9 <PID>` (force kill)
- **Monitor processes**:  
  `top` or `htop`
- **Start/stop a service**:  
  `sudo systemctl start|stop <service-name>`
- **Enable/disable a service**:  
  `sudo systemctl enable|disable <service-name>`

### User and Group Management
- **Add a user**:  
  `sudo useradd <username>`
- **Set user password**:  
  `sudo passwd <username>`
- **Delete a user**:  
  `sudo userdel <username>`
- **Add a group**:  
  `sudo groupadd <groupname>`
- **Add user to a group**:  
  `sudo usermod -aG <groupname> <username>`

### Permissions
- **Change file permissions**:  
  `chmod <permissions> <file-name>`  
  Example: `chmod 755 script.sh`
- **Change file ownership**:  
  `chown <user>:<group> <file-name>`
- **Change group ownership**:  
  `chgrp <group> <file-name>`

### Logs
- **View system logs**:  
  `journalctl` or `cat /var/log/messages`
- **Follow logs in real-time**:  
  `tail -f /var/log/<log-file>`

## Intermediate Commands

### Disk and Filesystem Management
- **Check filesystem type**:  
  `df -T`
- **Resize a filesystem**:  
  `sudo resize2fs <device>`
- **Check and repair filesystem**:  
  `sudo fsck <device>`
- **Mount/unmount a filesystem**:  
  `sudo mount <device> <mount-point>`  
  `sudo umount <mount-point>`
- **Create a swap file**:  
  ```
  sudo fallocate -l 1G /swapfile  
  sudo mkswap /swapfile  
  sudo swapon /swapfile
  ```

### Advanced Networking
- **Set a static IP**:  
  Edit `/etc/sysconfig/network-scripts/ifcfg-<interface>` and restart the network service.
- **Configure firewall (firewalld)**:  
  ```
  sudo firewall-cmd --zone=public --add-port=80/tcp --permanent  
  sudo firewall-cmd --reload
  ```
- **Check network traffic**:  
  `sudo tcpdump -i <interface>`
- **Test port connectivity**:  
  `nc -zv <hostname-or-ip> <port>`

### System Monitoring
- **Check disk I/O**:  
  `iostat`
- **Monitor memory usage**:  
  `vmstat 1`
- **Analyze disk usage**:  
  `sudo du -sh /*`

### Cron Jobs
- **Edit cron jobs**:  
  `crontab -e`
- **List cron jobs**:  
  `crontab -l`
- **Remove all cron jobs**:  
  `crontab -r`

## Advanced Commands

### Kernel and System Tuning
- **List loaded kernel modules**:  
  `lsmod`
- **Load/remove a kernel module**:  
  `sudo modprobe <module-name>`  
  `sudo modprobe -r <module-name>`
- **Check/modify kernel parameters**:  
  `sysctl -a`  
  `sudo sysctl -w <parameter>=<value>`

### SELinux Management
- **Check SELinux status**:  
  `sestatus`
- **Enable/disable SELinux**:  
  Edit `/etc/selinux/config` and set `SELINUX=enforcing` or `SELINUX=disabled`.
- **Change SELinux context**:  
  `chcon -t <context> <file-name>`
- **Restore default SELinux context**:  
  `restorecon <file-name>`

### LVM (Logical Volume Management)
- **List physical volumes**:  
  `pvs`
- **List volume groups**:  
  `vgs`
- **List logical volumes**:  
  `lvs`
- **Create a logical volume**:  
  `lvcreate -L <size> -n <lv-name> <vg-name>`
- **Extend a logical volume**:  
  `lvextend -L +<size> /dev/<vg-name>/<lv-name>`
- **Resize filesystem**:  
  `resize2fs /dev/<vg-name>/<lv-name>`

### Advanced Log Analysis
- **Filter logs by time**:  
  `journalctl --since "2023-10-01" --until "2023-10-02"`
- **Filter logs by priority**:  
  `journalctl -p err`
- **Monitor logs in real-time**:  
  `journalctl -f | grep "error"`

### Automation with Shell Scripting
- **Create a script**:  
  ```bash
  #!/bin/bash
  echo "Hello, World!"
  ```
- **Make a script executable**:  
  `chmod +x <script-name>.sh`
- **Run a script**:  
  `./<script-name>.sh`

## Miscellaneous
- **Compress a file/directory**:  
  `tar -czvf <archive-name>.tar.gz <file-or-directory>`
- **Extract a tar archive**:  
  `tar -xzvf <archive-name>.tar.gz`
- **Check command history**:  
  `history`
- **Clear terminal screen**:  
  `clear`
