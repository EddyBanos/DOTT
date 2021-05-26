
pipeline {
    agent { docker { image 'ruby:3.0.0' } } 
    triggers {
        pollSCM('* * * * *')
    }
    stages {
        stage("Requirements") {
            steps {
                echo "*******Installing requeriments************"
                sh 'gem install bundler -v 2.0.1'
            }
        }
         stage('Build') {
            steps {
                echo "**********Building stage**************"
                sh 'bundle install'
            }
        }
        stage('test') {
            steps {
                echo "**********Testing!**************"
                sh 'rake'
            }   
        }
        stage('SonarQube analysis') {
            steps {
               echo "Aqui va el analisis con SonarQube"
            }
        }
    }
}
