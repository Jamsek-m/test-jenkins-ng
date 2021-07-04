pipeline {
    // environment {
    // add env here
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
              git "${GIT_URL}"
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
          sh "printenv"
          sh "mvn -v"
          sh "java -version"
          sh "javac -version"
          sh "node -v"
          sh "npm -v"
        }
      }
    }
}
