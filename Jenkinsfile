pipeline {
    // environment {
    //
    // }

    agent any

    tools {
        nodejs "nodejs-12.4.0"
        maven "maven-3.6.1"
        jdk "jdk-12"
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
      stage("Testing") {
        steps {
          sh "mvn -v"
          sh "java -version"
          sh "javac -version"
          sh "node -v"
          sh "npm -v"
        }
      }
    }
}
