#Jenkins Installation 

#JDK11 
yum install java or jdk 11
yum install epel-release (for this package  we need download epel repo for this 
wget https://dl.fedoraproject.org/pub/epel-release-latest-7.noarch.rpm 
rpm -ivh epel-release-latest-7.noarch.rpm 

wget https://archives.jenkins-ci.org/redhat-stable/jenkins-2.303.1-1.1.noarch.rpm 

rpm -ivh jenkins-2.303.1-1.1.noarch.rpm 

systemctl start jenkins 
systemctl enable jenkins 
systemctl status jenkins 

#Jenkins Configurayion files
rpm -ql jenkins 
/etc/init.d/jenkins 
/etc/logrotate.d/jenkins
/etc/sysconfig/jenkins
/usr/lib/jenkins 
/usr/lib/jenkins/jenkins.war
/usr/sbin/rcjenkins
/var/cache/jenkins
/var/lib/jenkins
/var/log/jenkins 



#Download jenkis latest version  url
https://archives.jenkins-ci.org/redhat-stable/ 

systemctl stop jenkins 

Update the jenkins \

wget https://archives.jenkins-ci.org/redhat-stable/jenkins-2.8.1-1.1.noarch.rpm 

rpm -Uvh jenkins-2.303.1-1.1.noarch.rpm  --> Update the new jenkins version 

systemctl start jenkins 

systemctl status jenkins


Up
