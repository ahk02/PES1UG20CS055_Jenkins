pipeline {
  agent any
  stages {
    stage('Build') {
      sh 'g++ PES1UG20CS055.cpp -o PES1UG20CS055-1'
      build job: 'PES1UG20CS055-1'
    }
    stage('Test') {
      sh './PES1UG20CS055-1'
    }
  }
  post {
    failure {
      echo 'Pipeline Failed'
    }
  }
}
