pipeline {
    agent {
        docker { image 'rubi:2.6.1' }
    }
    stages {
        stage('Test') {
            steps {
                sh 'ruby -v'
            }
        }
    }
}
