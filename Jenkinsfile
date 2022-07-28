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
          sh "mvn package"
        echo 'build stage done'
      }
    }

  }
}
