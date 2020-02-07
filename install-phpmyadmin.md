# Install phpmyadmin

To get started, we will install phpMyAdmin from the default Ubuntu repositories.

This is done by  using the `apt` packaging system to pull down the files and install them on your system

```text
sudo apt install phpmyadmin php-mbstring php-gettext
```

This will ask you a few questions in order to configure your installation correctly.

{% hint style="danger" %}
 When the prompt appears, “apache2” is highlighted, but **not** selected. If you do not hit `SPACE` to select Apache, the installer will _not_ move the necessary files during installation. Hit `SPACE`, `TAB`, and then `ENTER` to select Apache.
{% endhint %}

* For the server selection, choose `apache2`
* Select `Yes` when asked whether to use `dbconfig-common` to set up the database
* You will then be asked to choose and confirm a MySQL application password for phpMyAdmin

Afterwards, restart Apache for your changes to be recognized:

```text
service apache2 restart
```

Normally we should now be able to reach phpmyadmin at this url [http://localhost/phpmyadmin](http://localhost/phpmyadmin)

But because of our configuration we need to create a symbolic link to phpmyadmin in our server root. We do that using this command

```text
ln -s /usr/share/phpmyadmin /var/www/html/admin/phpmyadmin
```

We should now be able to view the phpmyadmin login page at [http://localhost/phpmyadmin](http://localhost/phpmyadmin)



