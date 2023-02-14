pipeline {
  agent any
  stages {
    stage('Build') {
      steps {
        sh 'g++ PES1UG20CS055.cpp -o PES1UG20CS055-1'
        build job: 'PES1UG20CS055-1'
      }
    }
    stage('Test') {
      steps {
        sh './PES1UG20CS055-1'
      }
    }
    stage('Deploy') {
      steps {
        echo 'Deployment Successful'
      }
    }
  }
  post {
    failure {
      echo 'Pipeline Failed'
    }
  }
}
