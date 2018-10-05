FROM jenkins:latest

USER root

RUN apt-get update && apt-get install -y maven
RUN wget http://updates.jenkins-ci.org/download/war/2.138.1/jenkins.war
RUN mv ./jenkins.war /usr/share/jenkins
RUN chown jenkins:root /usr/share/jenkins/jenkins.war