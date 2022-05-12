pipeline {
    agent any

    stages {
        stage('Hello') {
            steps {
                echo 'Hello World'
            }
        }
        stage('Testing') {
            when {
                branch 'PR-*'
            }
            agent { label 'agent' }
            steps {
                sh './test.sh'
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