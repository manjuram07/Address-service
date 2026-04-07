pipeline {
    agent any

    stages {

        stage('Clone Code') {
            steps {
                git branch: 'main', git 'https://github.com/manjuram07/Address-service.git'
            }
        }

        stage('Build') {
            steps {
                sh 'mvn clean install'
            }
        }

        stage('Test') {
            steps {
                sh 'mvn test'
            }
        }

        stage('Package') {
                    steps {
                        sh 'mvn package'
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