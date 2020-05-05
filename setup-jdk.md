### Setup JDK 
#### Setup OpenJDK 8

	$ sudo apt install openjdk-8-jdk
  
#### Setup OracleJDK 8
After logging into your Oracle account, you can download JDK 8.
Then open up a terminal window and navigate to the download directory.
Then extract the tar.gz file to /usr/lib/jvm/ directory.

	$ sudo tar xvf jdk-8u221-linux-x64.tar.gz --directory /usr/lib/jvm/

Now we can check Java version.

	$ /usr/lib/jvm/jdk1.8.0_221/bin/java -version

Output:
	java version "1.8.0_221"
	Java(TM) SE Runtime Environment (build 1.8.0_221-b11)
	Java HotSpot(TM) 64-Bit Server VM (build 25.221-b11, mixed mode)

Check Java compiler version

	$ /usr/lib/jvm/jdk1.8.0_221/bin/javac -version

Output:
	javac 1.8.0_221

#### Set default JDK

Add JDK 8 to the alternatives system.

	$ sudo update-alternatives --install /usr/bin/java java /usr/lib/jvm/jdk1.8.0_221/bin/java 1
	$ sudo update-alternatives --install /usr/bin/javac javac /usr/lib/jvm/jdk1.8.0_221/bin/javac 1

Set a default JDK on Ubuntu 18.04/19.04, run the following command:

	$ sudo update-alternatives --config java

The available options will be listed.
You also need to do the same for Java compiler.

	$ sudo update-alternatives --config javac

Now you can run java -version and javac -version command to check the default JDK.

#### Uninstall JDK

So, first of all, check the vendor of the JDK you have installed on your system, whether it is Oracle JDK or Openjdk.
For that execute the following command in the terminal:

	$ java -version

If you have Oracle JDK installed then you will get the following result:

	anshuman@developer:~$ java -version
	java version "1.8.0_112"
	Java(TM) SE Runtime Environment (build 1.8.0_112-b15)
	Java HotSpot(TM) 64-Bit Server VM (build 25.112-b15, mixed mode)

Else if you have Openjdk installed then you will get the following result:

	anshuman@developer:~$ java -version
	java version "1.7.0_91"
	OpenJDK Runtime Environment (amzn-2.6.2.2.63.amzn1-x86_64 u91-b00)
	OpenJDK 64-Bit Server VM (build 24.91-b01, mixed mode)

Now follow the instructions below according to the JDK you have installed.

###### UNINSTALL ORACLE JDK
---Remove The Link
First of all remove the alternatives by executing the following commands:

	$ sudo update-alternatives --remove "java" "/usr/lib/jvm/jdk[version]/bin/java"
	$ sudo update-alternatives --remove "javac" "/usr/lib/jvm/jdk[version]/bin/javac"
	$ sudo update-alternatives --remove "javaws" "/usr/lib/jvm/jdk[version]/jre/bin/javaws"
Note: Replace the [version] with any version number that’s contained in jdk folder’s name. For example: jdk1.8.0_131.

---Remove The Package
After removing link, remove the package inside /usr/lib/jvm/jdk[version] by executing following command:

	$ sudo rm -r /usr/lib/jvm/jdk[version]

###### UNINSTALL OPENJDK

If you want to remove Openjdk only, execute the following command on terminal:

	$ sudo apt-get remove openjdk*

If you want to remove Openjdk along with dependencies, execute the following command on terminal:

	$ sudo apt-get remove --auto-remove openjdk*

If you want to remove Openjdk and it’s configuration files, execute the following command on terminal:

	$ sudo apt-get purge openjdk*

If you want to remove Openjdk along with dependencies and it’s configuration files, execute the following command on terminal:

	$ sudo apt-get purge --auto-remove openjdk*
	
