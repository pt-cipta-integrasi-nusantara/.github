pipeline {
    agent any
    stages {
        stage ('Build') {
            steps {
                sh 'echo Hello Build stage'
            }
        }
        stage ('Test') {
            steps {
                sh 'echo hello Test stage'
            }
        }
        stage('Back-end') {
            agent {
                docker { image 'maven:3.9.6-eclipse-temurin-17-alpine' }
            }
            steps {
                sh 'mvn --version'
            }
        }
    }
}
