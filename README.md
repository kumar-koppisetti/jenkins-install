# jenkins-install
# jenkins install from shell script


#!/bin/bash
sudo yum update -y
sudo yum upgrade -y
sudo amazon-linux-extras install java-openjdk11 -y
sudo yum install git -y
sudo wget -O /etc/yum.repos.d/jenkins.repo https://pkg.jenkins.io/redhat-stable/jenkins.repo
sudo rpm --import https://pkg.jenkins.io/redhat-stable/jenkins.io.key
sudo amazon-linux-extras install epel -y
sudo yum install jenkins -y
sudo systemctl start jenkins
sudo systemctl enable jenkins
sudo yum install maven -y
