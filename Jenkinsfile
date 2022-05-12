pipeline {
    agent any

    stages {
        stage('Hello') {
            steps {
                echo 'Hello World'
            }
        }
        stage('Secreto') {
            agent {label 'docker-agent'}
            steps {
                sh """
                    hostname
                    pwd
                    ls -la /
                """
            }
        }
    }
}