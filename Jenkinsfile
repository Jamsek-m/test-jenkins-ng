pipeline {
    // environment {
    //
    // }

    agent any

    tools {
        nodejs "nodejs-12.4.0"
    }

    stages {
        stage("cloning git") {
            steps {
                git "https://github.com/Jamsek-m/test-jenkins-ng"
            }
        }
        stage("npm install"){
          steps {
            sh "npm install"
          }
        }

        stage("Building Angular app") {
            steps {
                sh "npm run build"
            }
        }
        // dist/jenkins-ng
        stage("Building docker image") {
            steps {
                sh "docker -v"
            }
        }
    }
}
