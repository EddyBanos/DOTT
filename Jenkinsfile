pipeline {
    agent { docker { image 'ruby:3.0.0' } } 
    triggers {
        pollSCM('* * * * *')
    }
    stages {
        stage("Requirements") {
            steps {
                sh 'gem install bundler -v 2.0.1'
                echo "*******Installing requeriments************"
            }
        }
         stage('Build') {
            steps {
                sh 'bundle install'
            }
        }
        stage('test') {
            steps {
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
