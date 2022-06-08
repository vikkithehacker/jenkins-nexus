pipeline {
    agent any
    tools {
        maven "MAVEN"
    }
    stages {
        stage("Clone code from GitHub") {
            steps {
                script {
                    git branch: 'main', url: 'https://github.com/devopshint/jenkins-nexus';
                }
            }
        }
        stage("Maven Build") {
            steps {
                script {
                    sh "mvn clean package"
                }
            }
        }
          stage("Maven Build") {
            steps {
                script {
                    sh "mvn sonar:sonar -Dsonar.host.url=http://43.204.114.149:9000, -Dsonar.login=17099c39f304415783976e2e1c6fa4aae1715a77"
                }
            }
        }
        
