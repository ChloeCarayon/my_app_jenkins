node {
  try {
    stage('Environment') {
      sh 'git --version'
      sh 'docker -v'
      sh 'ls'
    }
    stage('Build Docker test'){
     sh 'docker build -t app-jenkins -f Dockerfile.test --no-cache .'
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
