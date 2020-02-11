# Install Mysql

Please run the following command  in order to install MySQL

```text
apt-get install mysql-server
```

Once Mysql is installed start the service using this command 

```text
service mysql start 
```

To connect to the MySQL Server, use this command:

```text
mysql -u root -p
```

At this point you will be asked for a password , as we have not set one up yet just hit enter to start the Mysql shell. Now to set a password for root user this command 

```text
UPDATE mysql.user SET authentication_string = PASSWORD('password') WHERE User = 'root';
```

To make the change take effect, reload the stored user information with the following command

```text
FLUSH PRIVILEGES;
```

