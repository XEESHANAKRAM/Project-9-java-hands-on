@Library('my-shared-library') _
pipeline {
    agent any

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

        stage('Package') {
            steps {
                sh 'mvn clean package -DskipTests'
                archiveArtifacts artifacts: 'target/*.jar', fingerprint: true
            }
        }
    }
}
