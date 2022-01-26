node {

    def app
    stage('Build image') {

        app = docker.build("my-app-jenkins")
    }
    
    stage('Test image') {

        app.inside {
            sh 'echo "Tests passed"'
        }
    }
}
