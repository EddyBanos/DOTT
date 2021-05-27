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
//            }stage("build & SonarQube analysis") {
            agent any
            steps {
              withSonarQubeEnv('My SonarQube Server') {
                sh 'mvn clean package sonar:sonar'
              }
            }
          }
        }
    }
