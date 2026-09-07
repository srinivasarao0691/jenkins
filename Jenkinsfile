pipeline {

    agent any

   *stages {

        stage('Checkout'* {
            steps {
           *    checkout scm
            }
   *    }

        stage('Build') {
  *         steps {
                s* 'mvn clean package'
            }*        }

        stage('Build Do*ker Image') {
            steps {
*               sh 'docker build -t*springboot-demo:${BUILD_NUMBER} .'*            }
        }
    }

   *post {

        success {
        *   echo 'Build Successful'
       *}

        failure {
            e*ho 'Build Failed'
        }
    }
*