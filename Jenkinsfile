node {
  try {
    stage('Environment') {
      sh 'git --version'
      sh 'docker -v'
    }
    stage('Build Docker test'){
     sh 'docker build -t app-jenkins .'
    }
    stage('Docker test'){
      sh 'docker run --rm app-jenkins'
    }
    stage('Clean Docker test'){
      sh 'docker rmi app-jenkins'
    }
    stage('Deploy'){
      if(env.BRANCH_NAME == 'master'){
        echo 'Here must deploy'
      }
    }
  }
  catch (err) {
    throw err
  }
}