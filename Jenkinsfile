@Library('my-shared-library') _
pipeline {
    agent any

    stages {
        stage('git') {
            steps {
                gitCheckout{
                    git branch: 'main', url: 'https://github.com/XEESHANAKRAM/Project-9-java-hands-on.git'
                }
                
            }
        }
    }
}
