node {
  stage('SCM') {
    checkout scm
  }
  stage('SonarQube Analysis') {
//    def scannerHome = tool 'SonarQube Scanner';
    withSonarQubeEnv() {
      sh "/opt/sonar-scanner-5.0.1.3006-linux/bin/sonar-scanner"
    }
  }
}
