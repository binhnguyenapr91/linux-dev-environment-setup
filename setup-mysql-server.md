### Setup MySql
On the screen of CLI  

	$ sudo apt-get install mysql-server mysql-common mysql-client
	$ sudo mysql_secure_installation
	$ sudo mysql -u root -p
	
After enter screen mysql  

	mysql> use mysql;
	mysql> select user,host,plugin from mysql.user;
	mysql> update user set plugin='mysql_native_password' where user='root';
	mysql> flush privileges;
	mysql> exit
	
Come back to CLI  

	$ service mysql restart

Login to MySqlServer
  $ mysql -u root
