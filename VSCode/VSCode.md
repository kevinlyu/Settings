# VSCode

## Issue

VisualStudioCode無法監視這個大型工作區的文件變化
   
    cat /proc/sys/fs/inotify/max_user_watches

    sudo vim /etc/sysctl.conf

    #Add this line
    fs.inotify.max_user_watches=524288

    sudo sysctl -p
