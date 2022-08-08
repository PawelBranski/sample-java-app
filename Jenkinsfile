
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

    stage('SonarQube analysis') {
      steps {
        sh "echo 'Zmienna SonarQube'"
        sh "whoami"
        def scannerHome = tool 'SonarQube';
        withSonarQubeEnv('sq1') { // If you have configured more than one global server connection, you can specify its name
        sh "${scannerHome}/bin/sonar-scanner"
        sh "koniec"
      }
      }
    }
  }
}
