node {
  stage('SCM') {
    checkout scm
  }
  stage('SonarQube Analysis') {
//    def scannerHome = tool 'SonarQube Scanner';
    withSonarQubeEnv() {
      sh "/opt/sonarqube/bin/linux-x86-64/sonar.sh console"
    }
  }
}
