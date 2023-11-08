First update the OS

yum update -y

Allow passwordAuthentication and permitrootlogin to do that

Go to sshd_config file

vim /etc/ssh/sshd_config

set line number using :se nu

uncomment permitrootlogin and change value to yes and give yes for password authentication

Restart and enable sshd

systemctl restart sshd
systemctl enable sshd

Change the password of root

passwd root

set the password

To install jenkins search in google jenkins installation on linux and copy the commands
______________________________________________________________________________
sudo wget -O /etc/yum.repos.d/jenkins.repo \
    https://pkg.jenkins.io/redhat-stable/jenkins.repo

sudo rpm --import https://pkg.jenkins.io/redhat-stable/jenkins.io-2023.key


sudo yum upgrade
# Add required dependencies for the jenkins package
sudo yum install fontconfig java-17-openjdk


sudo yum install jenkins


sudo systemctl daemon-reload
______________________________________________________________________________

sudo systemctl enable jenkins
sudo systemctl start jenkins
sudo systemctl status jenkins

______________________________________________________________________________

Copy the public ip of server and append :8080 to access jenkins dashboard

copy the path given on dashboard and give the path in server

cat <path>

copy the key and give it in the dashboard

install suggested plugins
And create user or you can continue as admin

Optional

To integrate git, install git

yum install git -y
git --version for versionof git

To use Maven as build tool, Install maven
yum install maven -y

and install maven plugin in jenkins

add maven in tools configuration by specifying the maven_home
we can get it by giving command 
mvn --version

create a webhook in git hub by using token from jenkins configure



