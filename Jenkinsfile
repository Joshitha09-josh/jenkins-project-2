pipeline {
    agent any

    stages {

        stage('Checkout') {
            steps {
                git branch: 'main',
                    url: 'https://github.com/Joshitha09-josh/jenkins-project-2.git'
            }
        }

        stage('Generate Report') {
            steps {
                bat 'python app.py'
            }
        }

        stage('Archive Report') {
            steps {
                archiveArtifacts artifacts: 'report.txt',
                                 fingerprint: true
            }
        }
    }
}
