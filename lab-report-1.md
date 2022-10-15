# Lab Report 1

## How to log onto a course specific account on ieng6

1. Installing VScode
* Go to the [Visual Studio code website](https://code.visualstudio.com/) and install the appropriate version for your OS.
* Upon opening VScode, you should see a page that looks like this: ![Vscode opening page](https://github.com/virsinghh/cse15l-lab-reports/blob/main/VScode%20opening.png?raw=true)


2. Remotely connecting
* First, look up your course-specific account at this [Link](https://sdacs.ucsd.edu/~icc/index.php)
* Next, open up a terminal in VScode and enter this command: `$ ssh cs15lfa22zz@ieng6.ucsd.edu`
* Remember to replace the "zz" in the command with your course-specific account letters.
* Type yes for the next message that pops up and press enter. Then, enter your password when prompted.
* Once you do this, you should be able to see the following interaction: ![Connecting remotely](https://github.com/virsinghhh/cse15l-lab-reports/blob/main/Screenshot%202022-10-14%20at%2011.20.42%20PM.png)

3. Trying some commands
* Try running various basic commands like pwd, ls, mkdir etc.
* Ensure that you try running these on both your machine and remotely on ieng6 after connecting via ssh.
* Here is a sample of what the commands should look like: ![Trying commands](https://github.com/virsinghhh/cse15l-lab-reports/blob/main/Screenshot%202022-10-14%20at%2011.21.30%20PM.png)

4. Moving files with scp
* Create a sample file on your computer to move using scp
* Then, in your terminal, select the directory where you saved the file and run the following command: `$ scp <filename> cs15lfa22zz@ieng6.ucsd.edu:~/`
* Enter your password when prompted to do so
* Next, log onto ieng6 again using ssh and use ls. You should be able to see the file you created on your machine.
* run it using javac java. It should look like this:![Moving files](https://github.com/virsinghhh/cse15l-lab-reports/blob/main/Screenshot%202022-10-14%20at%2011.29.18%20PM.png)

5. SSH keys
* ssh keys essentially help us login without having to always enter our password.
* On your machine type ssh-keygen in the terminal and hit enter for all the prompts that come up after. You should see your randomart: ![ssh-keygen](https://github.com/virsinghhh/cse15l-lab-reports/blob/main/Screenshot%202022-10-14%20at%2011.37.18%20PM.png)
* Log in to ieng6 using ssh again and run `mkdir .ssh` and then logout
* Once you're back on the client, run the following command: `$ scp /Users/<user-name>/.ssh/id_rsa.pub
cs15lfa22zz@ieng6.ucsd.edu:~/.ssh/authorized_keys`
* Use your username and the path seen above. It should look like this: ![ssh-keygen](https://github.com/virsinghhh/cse15l-lab-reports/blob/main/Screenshot%202022-10-14%20at%2011.37.38%20PM.png)

6. Optimizing remote running
* We can make this process smoother by combining commands and more.
* For example, if you add a command in quotes after ssh, it will run it directly on the remote server. 
* you can also combine statements with semicolons.
* An example: ![smooth remote running](https://github.com/virsinghhh/cse15l-lab-reports/blob/main/Screenshot%202022-10-14%20at%2011.38.52%20PM.png)

THE END

---
