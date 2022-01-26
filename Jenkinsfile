pipeline {
  agent any
  stages {
    stage('Environment') {
      sh 'git --version'
      sh 'docker -v'
      sh 'ls'
      sh "printenv"
    }
    stage('Build Docker test'){
     sh 'docker build -t app-jenkins -f Dockerfile --no-cache .'
    }
    stage('Docker test'){
      sh 'docker run --rm app-jenkins'
    }
    stage('Clean Docker test'){
      sh 'docker rmi app-jenkins'
    }
    stage('Deploy'){
      echo 'Here must deploy'
    }
  }
}