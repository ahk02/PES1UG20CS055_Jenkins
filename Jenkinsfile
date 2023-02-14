pipeline {
  agent any
  stages {
    stage('Build') {
      g++ PES1UG20CS055.cpp -o PES1UG20CS055-1 
    }
    stage('Test') {
      ./PES1UG20CS055-1
    }
  }
  post {
    failure {
      echo 'Pipeline Failed'
    }
  }
}
