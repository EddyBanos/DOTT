pipeline {
    agent any
    stages {
        stage("Compile") {
            steps {
                echo "Compile phase"
            }
        }
        stage("Unit test") {
            steps {
                echo "Unit test phase"
            }
        }
        stage("Code coverage") {
            steps {
        	    echo "Code coverage phase"
         	}
        }
//           steps {
//                withSonarQubeEnv('SonarQubePruebas') {
//                    sh './gradlew sonarqube'
//                }
//            }
        stage('SonarQube analysis') {
    withSonarQubeEnv(installationName: 'Sonarqube') { 
    }
         	}
        }
    }
