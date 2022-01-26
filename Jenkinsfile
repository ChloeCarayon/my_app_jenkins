pipeline {
  agent any
  stages {
    stage('Environment') {
      steps {
        sh 'git --version'
        sh 'docker -v'
        sh 'ls'
      }
    }
    stage('Build Docker test'){
      steps {
        sh 'docker build -t app-jenkins -f Dockerfile --no-cache .'
      }
      }
    stage('Docker test'){
      steps {
        sh 'docker run --rm app-jenkins'
      }
    }
    stage('Clean Docker test'){
      steps {
        sh 'docker rmi app-jenkins'
      }
    }
    stage('Deploy'){
      steps {
        echo 'Here must deploy'
      }
      
    }
  }
}
