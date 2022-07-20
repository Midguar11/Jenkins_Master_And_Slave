# Jenkins Master And Slave

- Open to Jenkins
- Manage Jenkins / Manage nodes and clouds
- New Node --> ( give name" winslave1 " ) --> selecect permanent agent --> ok
- Description ( Windows Slave 1)
- Remote root directory ( /home/username/jenkins )
- Usage ( Only build jobs with labels experssions matching this node)
- Launch method ( Launch agent via SSH )
- Host Give my public ip ( 111.111.111.111)
- Crendetials select setuped SSH Key
- Hots key Verification Strategy : " Known hosts file Verification Strategy "
- Availability: " Keep this Agent online as much as poosible "
- Save

# Slave setup

- Need Install JDK . Same version as master. When installed java setup JAVA HOME

      
      echo $JAVA_HOME
      JAVA_HOME='/usr/lib/jvm/java-8-openjdk-amd64/jre'
      PATH="$JAVA_HOME/bin:$PATH"
      export PATH
      echo $JAVA_HOME
      
- Install Maven

      wget https://mirrors.estointernet.in/apache/maven/maven-3/3.6.3/binaries/apache-maven-3.6.3-bin.tar.gz
      tar -xvf apache-maven-3.6.3-bin.tar.gz
      mv apache-maven-3.6.3 /opt/
      echo $M2_HOME

# More Setup JenkinsMaster
      
- Connect ssh to JenkinsMaster
- Change to root
            
      sudo su -
      cd /var/lib
      ls -la
      mkdir -p /var/lib/jenkins/.ssh
      ssh-keyscan -H slave_IP >> /var/lib/jenkins/.ssh/known_hosts
      cat /var/lib/jenkins/.ssh/known_hosts
      chown -R jenkins:jenkins /var/lib/jenkins/.ssh
      
 # Slave Setup
 
 - Connect SSH to Slave:
 
        sudo apt install acl
 
 
      
      
      
      
      
      
      





    

