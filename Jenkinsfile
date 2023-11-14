pipeline {
    agent any
    stages {
        stage('Build') {
            steps {
               sh '''
                sh build.sh
                '''
            }
        }
        stage('Test') {
            steps {
               sh '''
                sh test.sh
                '''
            }
        }
        stage('Deploy') {
            steps { 
                sh '''
                cat ./deploy.sh
                sh deploy.sh
                '''
            }
        }
    }
}