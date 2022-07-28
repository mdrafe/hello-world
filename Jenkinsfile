pipeline {
  agent any
  stages {
    stage('github clone') {
      steps {
        echo 'cloning repo'
        git(url: 'https://github.com/mdrafe/hello-world.git', branch: 'master', credentialsId: 'mdrafe549', poll: true)
      }
    }

    stage('maven build') {
      steps {
        dir(path: 'webapp') {
          sh '''$MAVEN_HOME/bin/mvn clean package
pwd'''
        }

        echo 'build stage done'
      }
    }

  }
}
