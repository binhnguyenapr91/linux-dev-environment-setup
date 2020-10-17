### Setup MySql
On the screen of CLI  

	$ sudo apt-get install mysql-server mysql-common mysql-client
	$ sudo mysql_secure_installation
	$ sudo mysql -u root -p
	
Come back to CLI  

	$ service mysql restart

Login to MySqlServer
  	
	$ mysql -u root
### Remove MYSQL
	sudo apt-get remove --purge mysql-[server|common|client]
	sudo apt-get purge mysql-[server|common|client]
	sudo apt-get autoremove
	sudo apt-get autoclean
	sudo apt-get remove dbconfig-mysql
	sudo apt-get dist-upgrade
