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
        stage('Checkout from shared lib') {
            steps {
                gitCheckout(repo: 'https://github.com/XEESHANAKRAM/Project-9-java-hands-on.git', branch: 'main')
            }
        }
        stage('Build & Test') {
            steps {
                mvnTest()
            }
        }
    }
}
