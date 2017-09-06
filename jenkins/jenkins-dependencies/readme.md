# Jenkins Requirements Readme
This is a simple readme outlining the requirements for Jenkins to
support this lab.

## Instructions to install Jenkins on CentOS VM
```
https://wiki.jenkins.io/display/JENKINS/Installing+Jenkins+on+Red+Hat+distributions
sudo wget -O /etc/yum.repos.d/jenkins.repo http://pkg.jenkins-ci.org/redhat/jenkins.repo
sudo rpm --import https://jenkins-ci.org/redhat/jenkins-ci.org.key
sudo yum install jenkins
sudo yum install java
```

## Jenkins with CentOS/RHEL based on openshift3/jenkins-2-rhel7
```
yum install -y wget net-tools iputils sshpass
wget https://dl.fedoraproject.org/pub/epel/epel-release-latest-7.noarch.rpm
rpm -i epel-release-latest-7.noarch.rpm
yum install -y python-devel python-pip gcc
pip install --upgrade pip
pip install ansible==2.3.2.0
pip install junos-eznc
pip install jxmlease
```

## Ubuntu based based on  library/jenkins:latest
```
apt-get update
apt-get install -y software-properties-common
apt-get install -y python-setuptools python-dev build-essential sshpass
easy_install pip
pip install ansible==2.3.2
pip install junos-eznc
pip install jxmlease
```
