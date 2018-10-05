Jenkins :

* Install sonarQube Scanner (https://docs.sonarqube.org/display/SCAN/Analyzing+with+SonarQube+Scanner+for+Jenkins)
* Manage jenkins > System configuration > SonarQube servers
* Manage jenkins > Global Tool Configuration > SonarQube Scanner

Jenkins update :

```
docker-compose exec -u root jenkins bash
apt-get update && apt-get install -y maven
wget http://updates.jenkins-ci.org/download/war/2.138.1/jenkins.war
mv ./jenkins.war /usr/share/jenkins
chown jenkins:root /usr/share/jenkins/jenkins.war
docker-compose restart jenkins
```

Jenkins plugins :

```
java -jar jenkins-cli.jar -s http://localhost:8080/ install-plugin
```

Docs :

* Jenkins java client : https://github.com/jenkinsci/java-client-api
* https://www.elastic.co/guide/en/elasticsearch/client/java-rest/6.3/java-rest-high-getting-started-initialization.html
* http://localhost:8080/pipeline-syntax/globals#currentBuild
* https://jenkins.io/doc/pipeline/steps/workflow-basic-steps/
* https://www.elastic.co/guide/en/elasticsearch/client/java-api/current/java-admin.html
