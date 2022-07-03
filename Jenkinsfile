//DECLARATIVE
pipeline {
    // agent any
    agent { docker { image 'maven:3.6.3' } }

    stages {
        stage('Build') {
            steps {
                sh "mvn --version"
                echo "Build"
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
