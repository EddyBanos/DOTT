pipeline {
    agent any
    stages {
        stage('Requirements') {
            agent {
                docker {
                    image 'ruby:2.6.1-4c4a'
                    reuseNode true
                }
            }
            steps {
                sh 'ruby -v'
                dir(path: 'cidr_convert_api/ruby/'){
                 echo "**********Building stage**************"
                 sh '''
                 ruby tests.rb
                 cp . /ruby-app
                 '''
            }
        }
         stage('Build') { 
             steps{
                 echo "**********Building stage**************"
            }
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
