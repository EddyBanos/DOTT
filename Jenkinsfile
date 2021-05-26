
pipeline {
    agent any
    triggers {
        pollSCM('* * * * *')
    }
    stages {
        stage("Requirements") {
            steps {
                echo "*******Installing requeriments************"
                
            }
        }
         stage('Build') {
            steps {
                echo "**********Building stage**************"
                sh '''
                apt-get install sudo
                   '''
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
