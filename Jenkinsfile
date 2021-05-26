
pipeline {
    agent any
    triggers {
        pollSCM('* * * * *')
    }
    stages {
        stage("Requirements") {
            steps {
                echo "*******Installing requeriments************"
                sh '''
                pwd
                ls
                   '''
            }
        }
         stage('Build') {
            steps {
                echo "**********Building stage**************"
            }
        }
        stage('test') {
            steps {
                echo "**********Testing!**************"
            }   
        }
        stage('SonarQube analysis') {
            steps {
               echo "Aqui va el analisis con SonarQube"
            }
        }
    }
}
