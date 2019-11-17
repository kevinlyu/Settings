# Virtualbox

## Reduce .vdi file size

Install zerofree

    sudo apt-get install zerofree


Reboot and enter rescue mode  in GRUB menu

    systemctl stop systemd-journald.socket 
    systemctl stop systemd-journald-dev-log.socket
    systemctl stop systemd-journald-audit.socket
    systemctl stop systemd-journald.service

    # swap off
    sudo swapoff -a 

    # remount as read-only mode 
    mount -n -o remount,ro -t ext4 /dev/sda1 / 

    zerofree /dev/sda1


In host OS (Windows 10)

    cd C:\Program Files\Oracle\VirtualBox
    
    .\VBoxManage.exe modifyvdi 'D:\VM\Ubuntu\Ubuntu 18.04.3 LTS\Ubuntu 18.04.3 LTS.vdi' -compact