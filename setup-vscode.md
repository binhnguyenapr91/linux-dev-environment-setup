#### OPTION 1

The repository and key can also be installed manually with the following script:

    $ curl https://packages.microsoft.com/keys/microsoft.asc | gpg --dearmor > packages.microsoft.gpg
    $ sudo install -o root -g root -m 644 packages.microsoft.gpg /usr/share/keyrings/
    $ sudo sh -c 'echo "deb [arch=amd64 signed-by=/usr/share/keyrings/packages.microsoft.gpg] https://packages.microsoft.com/repos/vscode stable main" > /etc/apt/sources.list.d/vscode.list'

Then update the package cache and install the package using:

    $ sudo apt-get install apt-transport-https
    $ sudo apt-get update
    $ sudo apt-get install code # or code-insiders

#### OPTION 2

The easiest way to install Visual Studio Code for Debian/Ubuntu based distributions is to download and install the .deb package (64-bit), either through the graphical software center if it's available, or through the command line with:

    $ sudo apt install ./<file>.deb

If you're on an older Linux distribution, you will need to run this instead:

    $ sudo dpkg -i <file>.deb
    $ sudo apt-get install -f # Install dependencies
    
Installing the .deb package will automatically install the apt repository and signing key to enable auto-updating using the system's package manager. Note that other binaries are also available on the VS Code download page.

#### OPTION 3

You can install it by running:

    $ sudo snap install --classic code # or code-insiders
