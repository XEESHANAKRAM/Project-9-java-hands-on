@Library('my-shared-library') _
pipeline {
    agent any
    options {
        disableConcurrentBuilds() // avoid conflicts
    }
    stages {
        stage('Cleanup') {
            steps {
                cleanWs()
            }
        }
        stage('Checkout from GitHub') {
            steps {
                git branch: 'main', url: 'https://github.com/XEESHANAKRAM/Project-9-java-hands-on.git'
            }
        }
        stage('Build & Test') {
            steps {
                sh 'mvn clean test'
            }
        }
    }
}
