
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
                cd cidr_convert_api/ruby
                junit tests.rb
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
