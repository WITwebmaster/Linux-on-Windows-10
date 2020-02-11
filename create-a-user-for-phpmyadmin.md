# Create a user for phpmyadmin

In the past you could use the Mysql root user to access Phpmyadmin but this has been closed off for security reasons since Mysql5.7. So we need to create a Mysql superuser that will allow us to login to Phpmyadmin

To create MySQL superuser  follow these steps:

1. At the command line, log in to MySQL as the root user:

   ```text
   mysql -u root -p
   ```

2. Type the MySQL root password, and then press Enter.
3. To create a superuser , type the following command. Replace _username_ with the user you want to create, and replace _password_ with the user's password:

   ```text
   GRANT ALL PRIVILEGES ON *.* TO 'username'@'localhost' IDENTIFIED BY 'password';
   ```

We now need to reset the database privileges

```text
FLUSH PRIVILEGES;
```

You should now be able to login to phpmyadmin and create a database

