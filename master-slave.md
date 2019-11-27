all in master:
   i want to build a pipeline
       requirements:
          maven
          sonarqube
          jfrog
          ansible
          terraform
to difficult manage all things in master
becuase all tools consume resouces, master might crash

example: 
  master linux machine
     java  (linux as node )
     .net -- .net work on windows (windows as  node)

  overcome this two problems by MASTER_SLAVE 
### Lab setup
 launch 2 ec2 instance ubuntu 16.04
   one is master (install jenkins)
   one machine for maven
        apt-get update
        apt-get install openjdk-8-jdk -y
        apt-get install maven -y
configure master-slave:
doing this things in all nodes and master
 create user jenkins   "adduser jenkins"
   enable passwordbase authentication   command "vi /etc/ssh/sshd_config"  
       passwdbaseauthentication no #please enable put yes
   give sudo permision to user "jenkins"
       visudo   "close with ctrl+x y enter"
     systemctl restart sshd
 ## do this thing only in master
   login into user
      su jenkins
    generate keys
       ssh-keygen
    copy this keys into all nodes
      ssh-copy-id usernameofnode@ipaddressofnode
      ex: ssh-copy-id jenkins@privateip
 ----------------------------------------------  
   goto manage jenkins
        manage nodes
           new node (give some name)
              

