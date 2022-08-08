pipeline {
  agent {
    docker {
      image 'maven:latest'
    }

  }
  stages {
    stage('build') {
      steps {
        echo '1st message'
      }
    }

    stage('test') {
      steps {
        sh 'echo "hi"'
      }
    }

    stage('sleep') {
      steps {
        sleep 3
      }
    }

  }
}