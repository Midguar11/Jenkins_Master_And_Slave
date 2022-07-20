# Jenkins Master And Slave

- Open to Jenkins
- Manage Jenkins / Manage nodes and clouds
- New Node --> ( give name" winslave1 " ) --> selecect permanent agent --> ok
- Description ( Windows Slave 1)
- Remote root directory ( /home/jenkins/jenkins-workspace )
- Usage ( Only build jobs with labels experssions matching this node)
- Launch method ( Launch agent via SSH )
- Host Give my public ip ( 111.111.111.111)

# Slave setup

- Need Install JDK . Same version as master. When installed java setup JAVA HOME

      
      echo $JAVA_HOME
      JAVA_HOME='/usr/lib/jvm/java-8-openjdk-amd64/jre'
      PATH="$JAVA_HOME/bin:$PATH"
      export PATH
      echo $JAVA_HOME
      
      


    

