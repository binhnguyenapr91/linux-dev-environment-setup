### Setup GIT

	$ sudo apt install git-all

Check git version

  	$ git --version
  
Git log tree setup
	
	git config --global alias.l "log --graph --all --pretty=format:'%C(yellow)%h%C(cyan)%d%Creset %s %C(white)- %an, %ar%Creset' -n 20"
