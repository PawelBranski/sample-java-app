node {
  stage('SCM') {
    git 'https://github.com/PawelBranski/sample-java-app'
  }
  stage('SonarQube analysis') {
    sh "echo 'Zmienna SonarQube'"
    sh "whoami"
    def scannerHome = tool 'SonarQube';
    sh "echo 'Line7 passed'"
    withSonarQubeEnv('sq1') { // If you have configured more than one global server connection, you can specify its name
      sh "${scannerHome}/bin/sonar-scanner"
    }
  }
}
