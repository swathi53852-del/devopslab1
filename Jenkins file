pipeline {
    agent any

    stages {

        stage('Build') {
            steps {
                bat 'javac HelloWorld.java'
            }
        }

        stage('Test') {
            steps {
                bat 'java HelloWorld'
            }
        }

        stage('Archive') {
            steps {
                archiveArtifacts artifacts: '*.class', fingerprint: true
            }
        }
    }
}
