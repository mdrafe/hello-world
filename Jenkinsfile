pipeline {
    agent any
    environment {
        GIT_HOME ="/usr/bin/git"
        JAVA_HOME ="/usr/lib/jvm/java-1.11.0-openjdk-amd64"
        MAVEN_PATH = "/usr/share/maven"
    }

    stages {
        stage('Git Clone'){
            steps {
                git url: 'https://github.com/GitPracticeRepo/spring-petclinic.git'
            }        
        }
        
        stage('Build') {
            steps {
                //sh "mvn clean install"
                sh "mvn package"
            }        
        }
        stage('msg') {
            steps {
                echo "Successfully Bbuild"
            }        
        }
    }        
}
