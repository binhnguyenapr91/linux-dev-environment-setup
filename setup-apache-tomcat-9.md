#### Step 1: Create the Tomcat Folder
Logged in as root

    $ mkdir ~/tomcat9
    $ cd tomcat9
    
#### Step 2: Install Tomcat
Next from your server, use wget command to download the tar to  the tomcat folder from the URL you copied in the previous step:  
    
    $ wget http://mirrors.viethosting.com/apache/tomcat/tomcat-9/v9.0.34/bin/apache-tomcat-9.0.34.tar.gz
    
    or
    
    $ curl -O http://www-eu.apache.org/dist/tomcat/tomcat-9/v9.0.30/bin/apache-tomcat-9.0.30.tar.gz
 
After the download completes, decompress the file in your tomcat folder:

    $ tar xvzf apache-tomcat-9.0.34.tar.gz
    
#### Step 3: Install Java Oracle JDK if not have JDK yet
    
#### Step 4: Configure .bashrc File
Set the environment variables in .bashrc with the following command:

    $ vim ~/.bashrc

Add this information to the end of the file:

    export JAVA_HOME=/usr/lib/jvm/jdk1.8.0_24
    export CATALINA_HOME=~/tomcat9/apache-tomcat-9.0.34

Save your edits and exit the .bashrc file, then run the following command to register the changes:

    $ . ~/.bashrc   
 
#### Step 5: Test Run
Tomcat and Java should now be installed and configured on your server. To activate Tomcat, run the following script:

    $CATALINA_HOME/bin/startup.sh

You should get a result similar to:

    Using CATALINA_BASE: /opt/tomcat
    Using CATALINA_HOME: /opt/tomcat
    Using CATALINA_TMPDIR: /opt/tomcat/temp
    Using JRE_HOME: /usr/lib/jvm/java-7-openjdk-amd64/
    Using CLASSPATH: /opt/tomcat/bin/bootstrap.jar:/opt/tomcat/bin/tomcat-juli.jar
    Tomcat started
    
To verify that Tomcat is working, visit the IP.of.your.server:8080 in a web browser. For example, http://127.0.0.1:8080.   
