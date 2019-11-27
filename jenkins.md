CICD:
   jenkins  -- cloud bees
   vsts     -- microsoft
   teamcity
   bamboo   -- atlsian
   circle ci
   code pipeline  -- aws
   travis
   git lab

installation:
-------------
  three ways of jenkins instalation
    1) standalone mode --java -jar jenkins.war   --not best practice
        1. take ubuntu 16.04 ec2 machine
        2.install java8  -- 
           apt-get update
           apt-get install openjdk-8-jdk -y
        3. download jenkins war file 
              http://mirrors.jenkins.io/war-stable/latest/jenkins.war
        4. java -jar jenkins.war  (if you pres ctrl+c  jenkins will stop)

   2) jenkins as a service    -- recomanded
      install java8
      wget -q -O - https://pkg.jenkins.io/debian/jenkins-ci.org.key | sudo apt-key add -
      sudo sh -c 'echo deb http://pkg.jenkins.io/debian-stable binary/ > /etc/apt/sources.list.d/jenkins.list'
       sudo apt-get update
      

sudo apt-get install jenkins


3) jenkins war deploy into tomcat
   /var/lib/tomcat/webapps


   project
      1 free style
      2 pipe line (groovy) 