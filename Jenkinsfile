
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
                cd cidr_convert_api/ruby
                ruby tests.rb
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
