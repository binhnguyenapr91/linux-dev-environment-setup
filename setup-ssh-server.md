### First update the system using the apt command or apt-get command:

    $ sudo apt update
    $ sudo apt upgrade

To install openssh-server package, run:
    
    $ sudo apt install openssh-server
    
### Verify that ssh service running
Type the following systemctl command:

    $ sudo systemctl status ssh

Check to confirm that OpenSSH server running on Ubuntu
If not running enable the ssh server and start it as follows by typing the systemctl command:

    $ sudo systemctl enable ssh
    $ sudo systemctl start ssh
