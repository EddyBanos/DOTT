pipeline {
    agent any
    stages {
        stage('Build') {
            agent {
                docker {
                    image 'rubi:2.6.1-4a4c'
                    // Run the container on the node specified at the top-level of the Pipeline, in the same workspace, rather than on a new node entirely:
                    reuseNode true
                }
            }
            steps {
                sh 'ruby -v'
            }
        }
    }
}
