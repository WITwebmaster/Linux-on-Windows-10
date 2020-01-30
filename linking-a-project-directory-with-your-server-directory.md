# Linking a project directory with your server directory

On the last page we found the Linux file system  in windows , but it is a hidden file and buried deep withing the windows folder structure.

 So to simplify our process we are going to create a working directory within windows and link that directory with your WSL Apache server. 

**Step 1:** We are going to make a directory for our files

```text
mkdir /mnt/c/Users/windows-user-name-here/Documents/webserver
```

**Step 2:** Now we are going to create a [Symbolic Link](https://linuxize.com/post/how-to-create-symbolic-links-in-linux-using-the-ln-command/) __to that folder 

```text
ln -s /mnt/c/Users/windows-user-name-here/Documents/webserver  /var/www/html
```

