@Library('my-shared-library') _
pipeline {
    agent any
    tools {
        jdk 'JDK'
        maven 'Maven-3.9'
    }
    stages {
        stage('Checkout from shared lib') {
            steps {
                gitCheckout(
                    repo: 'https://github.com/XEESHANAKRAM/Project-9-java-hands-on.git', 
                    branch: 'main'
                )
            }
        }

        stage('Build & Test') {
            steps {
                mvnTest()
            }
        }
    }
}
