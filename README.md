# Jenkins Master And Slave

- Open to Jenkins
- Manage Jenkins / Manage nodes and clouds
- New Node --> ( give name" winslave1 " ) --> selecect permanent agent --> ok
- Description ( Windows Slave 1)
- Remote root directory ( /var/jenkins )
- Usage ( Only build jobs with labels experssions matching this node)
- Launch method ( Launch agent via execution of command on the master )
- Host Give my public ip ( 111.111.111.111)

# TCP setup because allow inbound agents

- Manage Jenkins --> Configure Global Security
- Agents --> Inbound port --> Fix ( 50000)


# Back to agent setup

- Manage Jenkins / Manage nodes and clouds
- Select " winslave1 " --> Configure
- Launch Method " Launch agent by connecting it to the master " 
- Custom WorkDir path  " c:\1 "
- Save
On screen message 

" Run from agent command line:

curl -sO http://192.168.0.123:8080/jnlpJars/agent.jar
java -jar agent.jar -jnlpUrl http://192.168.0.123:8080/computer/winslave1/jenkins-agent.jnlp -secret 42f9ba3c9e66d70ce56c6e07-workDir "c:\1"

# Setup Agent Jenkins

- Copy url and open dowloads file: http://192.168.0.123:8080/jnlpJars/agent.jar
- Copy from dowloads agent.jarto  "c:\1 " 
- Run CMD and navigate c:\1 
- paste " java -jar agent.jar -jnlpUrl http://192.168.0.123:8080/computer/winslave1/jenkins-agent.jnlp -secret 42f9ba3c9e66d70ce56c6e07-workDir "c:\1" "
- Check the node look at the slave " status is runing "
- 

