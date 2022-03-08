# jenkins-install
jenkins install from shell script


#!/bin/bash
sudo yum update -y

sudo yum install git -y
sudo amazon-linux-extras install epel -y
sudo yum install maven -y
sudo yum remove java-17-amazon-corretto-headless-17.0.2+8-1.amzn2.1.x86_64 -y
sudo yum remove java-17-amazon-corretto-headless.x86_64 1:17.0.2+8-1.amzn2.1 -y
sudo wget -O /etc/yum.repos.d/jenkins.repo http://pkg.jenkins-ci.org/redhat-stable/jenkins.repo
sudo rpm --import https://pkg.jenkins.io/redhat-stable/jenkins.io.key
sudo yum install jenkins java-1.8.0-openjdk-devel -y
sudo yum install jenkins -y
sudo systemctl daemon-reload
sudo systemctl start jenkins
sudo systemctl enable jenkins
sudo systemctl status jenkins
