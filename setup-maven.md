### Install via apt
  
  sudo apt update
  sudo apt install maven
  
### Install latest version
  
  #### Install JDK
  #### Download maven
  
    wget https://www-us.apache.org/dist/maven/maven-3/3.6.3/binaries/apache-maven-3.6.3-bin.tar.gz -P /tmp
    
    sudo tar xf /tmp/apache-maven-*.tar.gz -C /opt
    
    sudo ln -s /opt/apache-maven-3.6.3 /opt/maven    
    
  #### Setup environment
  
    sudo nano /etc/profile.d/maven.sh
  
  Paste to file
  
    export JAVA_HOME=/usr/lib/jvm/default-java
    export M2_HOME=/opt/maven
    export MAVEN_HOME=/opt/maven
    export PATH=${M2_HOME}/bin:${PATH}
    
    sudo chmod +x /etc/profile.d/maven.sh
    
    source /etc/profile.d/maven.sh
