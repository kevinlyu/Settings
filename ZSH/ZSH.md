# ZSH

Install ZSH

    sudo apt-get install zsh
    sudo apt-get install powerline fonts-powerline

Install oh-my-zsh

    git clone https://github.com/robbyrussell/oh-my-zsh.git ~/.oh-my-zsh

Change default shell to zsh

    chsh -s /bin/zsh

Enable encoding support of Chinese character

    # Modify zsh.rc
    vim ~/.zshrc

    # Add in the buttom
    export LC_ALL=en_US.UTF-8  
    export LANG=en_US.UTF-8

    # Reload .zshrc
    source ~/.zshrc

## ZSH Themes

Go to [https://github.com/robbyrussell/oh-my-zsh/wiki/Themes](https://github.com/robbyrussell/oh-my-zsh/wiki/Themes)
and pick up theme you like

Then modify .zshrc configuration

    vim ~/.zshrc
    ZSH_THEME="THEME_NAME"

## Related Utils
Powerlevel9k zsh

    sudo apt-get install zsh-theme-powerlevel9k
    echo "source /usr/share/powerlevel9k/powerlevel9k.zsh-theme" >> ~/.zshrc

Highlighting support

    sudo apt-get install zsh-syntax-highlighting
    echo "source /usr/share/zsh-syntax-highlighting/zsh-syntax-highlighting.zsh" >> ~/.zshrc
