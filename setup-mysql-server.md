### Setup MySql
#### On the screen of CLI  

	$ sudo apt-get install mysql-server mysql-common mysql-client
	$ sudo mysql_secure_installation
	$ sudo mysql -u root -p
	
#### Come back to CLI  

	$ service mysql restart

#### Login to MySqlServer
  	
	$ mysql -u root
	
### Remove MYSQL

	sudo apt-get remove --purge mysql-[server|common|client]
	sudo apt-get purge mysql-[server|common|client]
	sudo apt-get autoremove
	sudo apt-get autoclean
	sudo apt-get remove dbconfig-mysql
	sudo apt-get dist-upgrade

### Change permisstion root account to login without sudo and password required
#### Login to mysql using sudo

	sudo mysql -u root -p
	
#### Use mysql

	UPDATE user SET plugin='mysql_native_password' WHERE User='root';
	FLUSH PRIVILEGES;

#### After this you can login to MySQL without sudo but there is no password set. So to give a password please do run below command.

	ALTER USER 'root'@'localhost' IDENTIFIED WITH mysql_native_password BY 'newpassword';

