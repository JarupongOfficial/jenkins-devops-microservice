//DECLARATIVE
pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
                echo 'Build'
            }
        }
        stage('DEV Test') {
            steps {
                echo 'DEV Test'
            }
        }
        stage('SIT Test') {
            steps {
                echo 'SIT Test'
            }
        }
    } post {
        always{
            echo 'Im awesome. I runs always'
        }
        success{
            echo 'I run when you are in the good mood. LOL!!!'
        }
        failure{
            echo 'You must be sad if you see me. LOL!!!'
        }
    }
}
