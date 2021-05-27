pipeline {
    agent any
    stages {
        stage("Requirements") {
            steps {
                echo "*******Installing requeriments************"
                
            }
        }
         stage('Build') {
           agent { 
             docker { 
             args '-v $HOME/jenkins:/ruby-app image 'ruby:2.6.1' }
             steps {
               dir(path: 'cidr_convert_api/ruby/'){
                 echo "**********Building stage**************"
                 sh '''
                 ruby tests.rb
                 cp . /ruby-app
                 '''
               }
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

