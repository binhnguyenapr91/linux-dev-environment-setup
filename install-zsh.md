### Install prerequisite packages. 
    apt install zsh
    
### Check zsh version
    zsh --version
    
### Change default shell to zsh
    chsh -s $(which zsh)
    
### Check default shell
    echo $SHELL
    
### Install Oh My Zsh. 
    sh -c "$(curl -fsSL https://raw.githubusercontent.com/robbyrussell/oh-my-zsh/master/tools/install.sh)"

### Get the “Powerline” fonts required for a fancy theme. 
    sudo apt install fonts-powerline  

### Set up a fancy theme. 
    Open up ~/.zshrc and change ZSH_THEME variable: ZSH_THEME="agnoster"
