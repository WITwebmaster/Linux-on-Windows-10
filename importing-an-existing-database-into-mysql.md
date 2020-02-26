# Importing an existing database into mysql

Once you have your development environment setup you may want to import different versions of your database into mysql . There are two ways you can do this 

### **By Phpmyadmin**

If you have a small database you can do this easily bay creating a new blank database  , then going to import and selecting the .sql file you want to import . There is a size limit of 200mb on the import but in my experience larger Databases above 100mb sometimes have issues using this method.If you database is larger that 100mb I suggest you user the command-line method documented below 

![](.gitbook/assets/en_choose-file-to-import.png)

### Command-line method 

So to use the command line method you need a blank database which you can create in phpmyadmin or using the mysql command

```text
CREATE DATABASE databasename; 
```

Now copy you .sql backup file to one of your webserver directories and then **cd** to that directory in command-line 

Now use this command to import the sql file 

```text
mysql -u username -p database_name < dumpfilename.sql
```

So the username can be root or the a mysql superuser , the database is the name of the blank database you have created and the dumpfilename is the mysql backup file

You will be then prompted for your password and it should go to a flashing prompt as it imports the database 







