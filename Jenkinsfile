pipeline {

    agent any

    tools {
            maven 'Maven-3.9'
    }

    stages {

        stage('Checkout') {
            steps {
                checkout scm
            }
        }

        stage('Build') {
            steps {
                sh 'mvn clean package'
            }
        }


        stage('Build Docker Image') {
            steps {
                sh 'docker build -t springboot-demo:${BUILD_NUMBER} .'
            }
        }

    }

    post {

        success {
            echo 'Build Successful'
        }

        failure {
            echo 'Build Failed'
        }

    }
}
