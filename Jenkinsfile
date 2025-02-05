pipeline {
    agent any
    stages {

        stage('pull') {
            steps {
                git branch: 'main', url: 'https://github.com/PraveenKuber/Amazon-Jenkins.git'
            }
        }
        stage('compile') {
            steps {
                sh 'mvn compile'
            }
        }


        
        stage('build') {
            steps {
                 sh 'mvn clean install'
            }
        }

    }

    post {
        always {
            echo 'This runs regardless of build result'
        }
        success {
            echo 'Build success'
        }
        failure {
            echo 'Failure in the build'
        }
    }

}
