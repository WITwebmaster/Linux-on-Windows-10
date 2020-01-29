# Sudo and root user

 When you work with a form of Linux,  quickly encounter the **'sudo'** command and the term **'root'**, but what is sudo / root? 

#### Root

A Linux server has a root user, which you can compare with the administrator on a Windows computer. This root user has full access and rights to the operating system of your server by default

#### Sudo

Many [command-line commands](https://www.transip.eu/knowledgebase/entry/594-want-to-use-commandline-ssh//?utm_source=knowledge%20base) can only be executed by a root user. However, if you work via [SSH](https://www.transip.eu/knowledgebase/entry/594-want-to-use-commandline-ssh//?utm_source=knowledge%20base) or  you will usually be logged in as a different user at first. 

To be able to execute commands as root user as this \(non-root\) user, the **'Sudo'** command is used, which stands for **'super user do'**. 

You use **'sudo'** by placing it in front of the command you want to execute, for example

```text
sudo nano /var/log/example
```

The root user’s password is then requested before the command is actually executed. The password is remembered for 15 minutes. During this time you won't be prompted again for your password

### Switching to the root user <a id="switching_to_the_root_user"></a>

You can switch from a regular user to the root user. Thereafter, you do not have to place **'sudo'** in front of the commands that you execute. Because we are running this setup on a local machine and we are not worried about the security  we will run all of our commands at root . To switch to the root user use this command 

```text
sudo su
```

 With the **'exit'** command, you switch back to your user account

