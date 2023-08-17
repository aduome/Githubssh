# Setting up SSH access to GitHub
SSH provides a secure way to connect to remote servers and services like GitHub without using usernames and passwords. It uses key-based authentication instead.

This guide covers how to generate SSH keys and connect to GitHub repositories from your local machine via SSH.
## Prerequisites
- You need to have Git installed and configured on your local machine.
- You need a GitHub account.
- You need to be working from the command line interface (CLI) on your local system.

## Generate SSH keys
To setup SSH access to GitHub, you need to generate a new SSH key pair.

Open your CLI and enter the following:
~~~
ssh-keygen -t ed25519 -C "your_email@example.com"
~~~

This will initiate the key generation process. When prompted, press Enter to save the key in the default location.

Enter a secure passphrase when prompted.

This will generate a public key (id_ed25519.pub) and a private key (id_ed25519), stored in the ~/.ssh directory on your machine.
## Add SSH key to GitHub
Next, you need to add your new public key to your GitHub account.

Copy the contents of the id_ed25519.pub file.

In GitHub, go to Settings > SSH and GPG keys. Click New SSH key.

Paste the copied key and click Add SSH key.

You now have an SSH key associated with your GitHub account.
## Clone GitHub repository via SSH
To clone a GitHub repo using the SSH URL:
~~~
git clone git@github.com:user/repo.git
~~~
Enter your passphrase when prompted.

This authenticates you and provides access to clone via SSH.

The repository will be cloned onto your local machine.
## Conclusion
You have now set up SSH access to GitHub by generating a key pair and associating the public key with your GitHub account. Repositories can be efficiently cloned and accessed securely over SSH.
