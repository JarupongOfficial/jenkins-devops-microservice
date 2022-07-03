//DECLARATIVE
pipeline {
    agent any
    // agent { docker { image 'maven:3.6.3' } }
    // agent { docker { image 'node:13.8' } }

    environment {
        dockerHome = tool 'myDocker'
        mavenHome = tool 'myMaven'
        PATH = "$dockerHome/bin:$mavenHome/bin:$PATH"
    }

    stages {
        stage('Checkout') {
            steps {
                sh 'mvn --version'
                sh 'docker --version'
                echo 'Build'
                echo "PATH - $PATH"
                echo "BUILD NUMBER - $env.BUILD_NUMBER"
                echo "BUILD_ID - $env.BUILD_ID"
                echo "JOB_NAME - $env.JOB_NAME"
                echo "BUILD_TAG - $env.BUILD_TAG"
                echo "BUILD_URL - $env.BUILD_URL"
            }
        }
        stage('Compile') {
            steps {
                sh 'mvn clean compile'
            }
        }
        stage('DEV Test') {
            steps {
                sh 'mvn test'
            }
        }
        stage('SIT Test') {
            steps {
                sh 'mvn failsafe:integration-test failsafe:verify'
            }
        }
    }
    post {
        always {
            echo 'Im awesome. I runs always'
        }
        success {
            echo 'I run when you are in the good mood. LOL!!!'
        }
        failure {
            echo 'You must be sad if you see me. LOL!!!'
        }
        changed {
            echo 'You mood is unstable. Keep calm and take a look!!!'
        }
    }
}
