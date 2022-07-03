//DECLARATIVE
pipeline {
    agent any
    // agent { docker { image 'maven:3.6.3' } }
    // agent { docker { image 'node:13.8' } }


    stages {
        stage('Build') {
            steps {
                // sh "mvn --version"
                // sh "node --version"
                echo "Build"
                echo "PATH - $PATH"
                echo "BUILD NUMBER - $env.BUILD_NUMBER"
                echo "BUILD_ID - $env.BUILD_ID"
                echo "JOB_NAME - $env.JOB_NAME"
                echo "BUILD_TAG - $env.BUILD_TAG"
                echo "BUILD_URL - $env.BUILD_URL"
            }
        }
        stage('DEV Test') {
            steps {
                echo "DEV Test"
            }
        }
        stage('SIT Test') {
            steps {
                echo "SIT Test"
            }
        }
    }
    post {
        always {
            echo "Im awesome. I runs always"
        }
        success {
            echo "I run when you are in the good mood. LOL!!!"
        }
        failure {
            echo "You must be sad if you see me. LOL!!!"
        }
        changed {
            echo "You mood is unstable. Keep calm and take a look!!!"
        }
    }
}
