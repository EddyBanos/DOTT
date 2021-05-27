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
        stage('SonarQube analysis') {
//           steps {
//                withSonarQubeEnv('SonarQubePruebas') {
//                    sh './gradlew sonarqube'
//                }
//            }
            steps {
                echo "SonarQube analysis phase"
        	    withSonarQubeEnv('Sonarqube', envOnly: true) {
                    println ${env.SONAR_HOST_URL} 
                }
         	}
        }
    }
}
