node {
  stage('SCM') {
    checkout scm
  }
  stage('SonarQube Analysis') {
//    def scannerHome = tool 'SonarQube Scanner';
    withSonarQubeEnv() {
      sh "/opt/sonar-scanner-5.0.1.3006-linux/bin/sonar-scanner -Dsonar.host.url=http://172.31.6.142:9000 -Dsonar.login=sqa_f7e409defd5ce51cafafe2bcd658d5ed0b77aaf6 -Dsonar.projectKey=NodeJS_Project"
    }
  }
}
