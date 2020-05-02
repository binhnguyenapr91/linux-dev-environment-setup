#### Checking for existing SSH keys  

Before you generate an SSH key, you can check to see if you have any existing SSH keys.

Open Terminal.

Enter ls -al ~/.ssh to see if existing SSH keys are present:

    $ ls -al ~/.ssh 
    
Lists the files in your .ssh directory, if they exist
Check the directory listing to see if you already have a public SSH key.
By default, the filenames of the public keys are one of the following:

    id_rsa.pub
    id_ecdsa.pub
    id_ed25519.pub
    
If you don't have an existing public and private key pair, or don't wish to use any that are available to connect to GitHub,
then generate a new SSH key.

If you see an existing public and private key pair listed (for example id_rsa.pub and id_rsa) that you would like to use to connect to GitHub, you can add your SSH key to the ssh-agent.

#### Generating a new SSH key

Open Terminal.

Paste the text below, substituting in your GitHub email address.

    $ ssh-keygen -t rsa -b 4096 -C "your_email@example.com"
    
This creates a new ssh key, using the provided email as a label. Generating public/private rsa key pair.  
When you're prompted to "Enter a file in which to save the key," press Enter. This accepts the default file location.  
Enter a file in which to save the key (/home/you/.ssh/id_rsa): [Press enter]  
At the prompt, type a secure passphrase. For more information, see "Working with SSH key passphrases".  
Enter passphrase (empty for no passphrase): [Type a passphrase]  
Enter same passphrase again: [Type passphrase again]  

#### Adding your SSH key to the ssh-agent

Before adding a new SSH key to the ssh-agent to manage your keys, you should have checked for existing SSH keys and generated a new SSH key. 
Start the ssh-agent in the background.  

    $ eval "$(ssh-agent -s)"
   > Agent pid 59566
   
Add your SSH private key to the ssh-agent. If you created your key with a different name, or if you are adding an existing key that has a different name, replace id_rsa in the command with the name of your private key file.

    $ ssh-add ~/.ssh/id_rsa  
    
#### Add the SSH key to your GitHub account.
