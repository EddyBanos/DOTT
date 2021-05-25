pipeline {
    agent any
    triggers {
        pollSCM('* * * * *')
    }
    stages {
        stage("Compile") {
            steps {
                echo "La parte compilada"
            }
        }
        stage("Unit test") {
            steps {
                echo "La parte del test"
            }
        }
        stage("Code coverage") {
            steps {
        	    echo "Code coverage"
         	}
        }
        stage('SonarQube analysis') {
            steps {
                withSonarQubeEnv('SonarQubePruebas') {
                    sh './gradlew sonarqube'
                }
            }
        }
    }
}