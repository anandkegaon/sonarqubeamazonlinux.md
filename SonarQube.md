SonarQube installation steps and requirment are as follows.

Server requirment :

t2.medium
java 8
sonarqube 7.6 
open 9000 port in the server.

installation steps:

login using root user .

    sudo su

Install JAVA using below command.(version 1.8).

    sudo yum install java-1.8.0 -y

Download the sonarzip file by below link in (/opt folder - optional) .   

    wget https://binaries.sonarsource.com/Distribution/sonarqube/sonarqube-7.6.zip

Unzip the file using below command .

     sudo unzip sonarqube-7.6.zip 

Creat new user name called sonar .

     groupadd sonar

 Give sudo permission using below command .  

    visudo

    root ALL=ALL  ALL
    sonar ALL=ALL NOPASSWD=ALL

su - sonar (switch user to sonar)

Open the folder where the sonarqube is installed 

      cd bin/linux-x86-64

 run below command.

     ./sonar.sh start    // start the sonar 
     ./sonar.sh status   // check the status of sonar

#### login using public ip:9000 to browse the sonarqube.
   
    
