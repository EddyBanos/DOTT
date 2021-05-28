
pipeline {
  //agent {
    //label 'docker' 
 // }
  agent any
  stages {
    stage('Installing tools'){
      steps{
        echo "Installing tools"
      }
    }
    stage('Building '){
      steps{
        echo "Building"
      }
    }
        stage('Unit Test '){
      steps{
        echo "*******Testing*******"
          }
        }
       stage('SonarQube analysis') {
            steps {
               echo "Aqui va el analisis con SonarQube"
            }
        }
     }
    }
/*    agent {
      docker{
        label 'docker'
        image 'ruby'
        args '--name ruby'
      }
    }*/
    /*steps {
        sh 'gpg --keyserver hkp://pool.sks-keyservers.net --recv-keys 409B6B1796C275462A1703113804BB82D39DC0E3 7D2BAF1CF37B13E2069D6956105BD0E739499BDB'
      sh' curl -sSL https://get.rvm.io | bash -s stable --ruby'
      */
