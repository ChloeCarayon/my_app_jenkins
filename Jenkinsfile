pipeline {
    agent any
    tools {nodejs "NodeConfig"}

    agent { dockerfile true }


    stages {
//            stage('Cloning Git'){
//                 steps {
//                    git([url:'https://github.com/KHEfreiIntervenant/it_for_managers_backend.git', branch: 'main'])
//                }
//               
//
//            }
            stage('Npm Build'){
                steps {
//                    sh "npm install"
//                    sh "npm start"
			sh "echo test"  
              }
            }

        stage('Test') {
            steps {
                sh 'node --version'
                sh 'svn --version'
            }
        }
        
    }
}

