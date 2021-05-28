
pipeline {
agent any
stages {
 //stage("Code Checkout from GitLab") {
  //steps {
   //git branch: 'master',
    //credentialsId: 'gitlab_access_token',
    //url: 'http://your-ip-here:10080/root/test-project.git'
  //}
 //}
   stage('Code Quality Check via SonarQube') {
   steps {
       script {
       def scannerHome = tool 'sonarqube';
           withSonarQubeEnv("Sonarqube") {
           sh "${tool("sonarqube")}/bin/sonar-scanner \
           -Dsonar.projectKey=DevOpsRubyTest \
           -Dsonar.sources=. \
           -Dsonar.css.node=. \
           -Dsonar.host.url=http://3.233.252.206:9000 \
           -Dsonar.login="4346c1bbc5f66983e2ba3b76033e5e8308bcd36d"
               }
           }
       }
   }
   stage("Install Project Dependencies") {
   steps {
       echo "**********Install Project***********"
       }
   }
}
}
