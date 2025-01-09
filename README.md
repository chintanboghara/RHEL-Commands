## System Information

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

## Package Management (YUM/DNF)

- **Install a package**:  
  `sudo yum install <package-name>`  
  or  
  `sudo dnf install <package-name>`

- **Remove a package**:  
  `sudo yum remove <package-name>`  
  or  
  `sudo dnf remove <package-name>`

- **Update all packages**:  
  `sudo yum update`  
  or  
  `sudo dnf update`

- **Search for a package**:  
  `sudo yum search <keyword>`  
  or  
  `sudo dnf search <keyword>`

- **List installed packages**:  
  `rpm -qa`

## File Management

- **List files in a directory**:  
  `ls -l`

- **Create a directory**:  
  `mkdir <directory-name>`

- **Remove a file**:  
  `rm <file-name>`

- **Remove a directory**:  
  `rm -r <directory-name>`

- **Copy a file**:  
  `cp <source> <destination>`

- **Move or rename a file**:  
  `mv <source> <destination>`

- **View file content**:  
  `cat <file-name>`

- **Edit a file with nano**:  
  `nano <file-name>`

- **Edit a file with vi/vim**:  
  `vi <file-name>`  
  or  
  `vim <file-name>`

## Networking

- **Check IP address**:  
  `ip addr show`  
  or  
  `ifconfig`

- **Ping a host**:  
  `ping <hostname-or-ip>`

- **Check network connectivity**:  
  `curl <URL>`  
  or  
  `wget <URL>`

- **View open ports**:  
  `netstat -tuln`

- **Restart network service**:  
  `sudo systemctl restart network`

## User Management

- **Create a new user**:  
  `sudo adduser <username>`

- **Delete a user**:  
  `sudo userdel <username>`

- **Change user password**:  
  `sudo passwd <username>`

- **Switch user**:  
  `su - <username>`

- **Add user to sudoers**:  
  `sudo usermod -aG wheel <username>`

## Service Management (systemd)

- **Start a service**:  
  `sudo systemctl start <service-name>`

- **Stop a service**:  
  `sudo systemctl stop <service-name>`

- **Restart a service**:  
  `sudo systemctl restart <service-name>`

- **Enable a service to start on boot**:  
  `sudo systemctl enable <service-name>`

- **Disable a service from starting on boot**:  
  `sudo systemctl disable <service-name>`

- **Check service status**:  
  `sudo systemctl status <service-name>`

## Logs

- **View system logs**:  
  `journalctl`

- **View logs for a specific service**:  
  `journalctl -u <service-name>`

- **View last 100 log entries**:  
  `journalctl -n 100`

- **Follow logs in real-time**:  
  `journalctl -f`

## Firewall (firewalld)

- **Check firewall status**:  
  `sudo firewall-cmd --state`

- **Allow a service through the firewall**:  
  `sudo firewall-cmd --add-service=<service-name> --permanent`

- **Allow a port through the firewall**:  
  `sudo firewall-cmd --add-port=<port-number>/tcp --permanent`

- **Reload firewall rules**:  
  `sudo firewall-cmd --reload`

- **List all allowed services/ports**:  
  `sudo firewall-cmd --list-all`

## Miscellaneous

- **Find a file**:  
  `find / -name <filename>`

- **Search for a string in files**:  
  `grep "search-term" <file-name>`

- **Compress a file/directory**:  
  `tar -czvf <archive-name>.tar.gz <file-or-directory>`

- **Extract a tar.gz file**:  
  `tar -xzvf <archive-name>.tar.gz`

- **Check running processes**:  
  `ps aux`

- **Kill a process**:  
  `kill <PID>`  
  or  
  `kill -9 <PID>` (force kill)

- **Schedule a cron job**:  
  `crontab -e`

- **Check disk space usage**:  
  `du -sh <directory>`
