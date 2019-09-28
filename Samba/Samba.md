# Samba for Ubuntu

## Install & Configure
Install Samba
    
    sudo apt-get install samba

Check if Samba works

    # port 137, 138, 139 should be listened 
    sudo netstat -tulnp | grep -e '[sn]mbd'

Samba setting file

    # Backup
    cd /etc/samba
    sudo cp smb.conf smb.conf.backup
    sudo vim smb.conf

    # Add contents below
    [share]                                    
    comment    = Temporary file space
    path       = /home/kevin
    writable   = yes
    browseable = yes

    # Restart Samba service
    sudo service smbd restart

## Issues
Windows access denied

    #Open Windows cmd
    # See if there is an existing connection
    net use

    # delete the connection
    net use \\172.21.69.2\user /delete

## References
- https://magiclen.org/ubuntu-server-samba/
- https://blog.xuite.net/mypace/wretch/145109090-%5B%E9%9B%BB%E8%85%A6%5D+%E6%B8%85%E9%99%A4%E9%80%A3%E7%B7%9A%E5%85%B1%E7%94%A8%E8%B3%87%E6%BA%90%E5%B8%B3%E6%88%B6%E7%9A%84%E8%B3%87%E8%A8%8A