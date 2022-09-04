
## Project Goal:

To implement a CI/CD pipeline using Jenkins, Maven and Git.

![](./plan.jpg)


## Source Code:

Source code taken from https://github.com/yankils/hello-world.


## Setting the Jenkins Server:

* First an ec2 instance in the AWS has been created.

![](instance.png)

* MobaXterm has been used for creating remote sessions.
* Added the keypair that was generated for the instance to the private key option in the advanced 
  ssh settings.

![](MobaXterm.png)

* Got the centos/redhat LTS version of Jenkins. Link: https://pkg.jenkins.io/redhat-stable/  
* Installed the epel releases using amazon-linux-extras instead of sudo.(Amazon linux was selected in the ec2 instance)
  : 'amazon-linux-extras install epel'
* Installed java-openJDK11 ( 'amazon-linux-extras install java-openJDK11' )
* Installed jenkins 'yum install jenkins'
* Start the jenkins server: 'service jenkins start'
* To access the UI version of Jenkins, grabbed the public IPv4 adress of the instance and 
  routed it to port 8080.

![](./Jenkin's_Ready.png)

![](./Jenkin's_DashBoard.png)


## Integrating Git with Jenkins

* Installed git: 'yum install git'
* Installed Github plugin from the pluggin manager in the Jenkins UI.(from the available section).

![](./Github_Pluggin.png)




## Running Jenkins job to pull code from Github

![](./Github_pull.png)
## Integrating Maven with Jenkins
* Installed Maven using wget command. Link:https://maven.apache.org/download.cgi
* Setting up environmental variables:

![](Setting_Envs.png)

* Installed Maven pluggin:

![](Maven_Pluggin.png)




## Building the project with Jenkins

![](./Maven_Project.png)