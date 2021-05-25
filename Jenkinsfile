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
                echo "Aqui va la parte del unit test"
            }
        }
        stage("Code coverage") {
            steps {
        	    echo "Code coverage"
         	}
        }
        stage('SonarQube analysis') {
            steps {
               echo "Aqui va el analisis con SonarQube"
            }
        }
    }
}
