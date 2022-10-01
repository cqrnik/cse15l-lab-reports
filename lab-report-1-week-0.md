
# Lab Report 1


## Installing VS Code

- Go to the [Visual Studio Code website] (https://code.visualstudio.com/), and follow the guide for your specific device
- Run the installer, and install the program in the required directory.

![Image](images/background.png)

## Remotely Connecting

- If on a Windows computer, install the OpenSSH client to connect to a remote computer
- Open a terminal and run the following command with your course specific account name:
`$ ssh cs15lfa22zz@ieng6.ucsd.edu`
- If the command is run for the first time, read the prompt and type 'yes'
- Enter the password
- A successful connection should look something like this

## Trying Some Commands
- Commands can be run on both a local terminal and a remote one, sometimes with varying results.
- Try using `ls` to list out the files in the current directory
- Use `mkdir <directory>` to make a new directory with any name, and `cd <directory>` to change to this new directory
- The `cat` command concatenates multiple files and prints them. In the screenshot you can see that there is no 
file in the location given, so nothing is printed.

## Moving Files with scp
- `scp` stands for secure copy, and can be used to copy local files to a remote computer
- Run the command `scp <filename> <account name>:~` from the local terminal to copy the file into the home directory
- Enter the password, and the file will be copied
- Log in to the remote terminal, and run the file

## Setting an SSH Key
- First, log in to the remote terminal and run `mkdir .ssh`
- On the local terminal, run `ssh-keygen`, and press enter again to take the default path
- Use scp to copy the generated public key from the local client to the .ssh directory of the remote computer
`scp /Users/<username>/.ssh/id_rsa.pub <account name>:~/.ssh/authorized_keys`
- You should now be able to log in without using a password


## Optimizing Remote Running
- Semicolons (;) can be used to run multiple commands in one line
- The up arrow key can be used to access a previous terminal command
- If all the steps to update a file are in one line, they can be accessed with a single up arrow keystroke

