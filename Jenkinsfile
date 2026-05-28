pipeline {
    agent any

    stages {

        stage('Clone') {
            steps {
                git 'https://github.com/YOUR_USERNAME/jenkins-demo.git'
            }
        }

        stage('Build') {
            steps {
                sh './build.sh'
            }
        }
    }

    post {
        success {
            archiveArtifacts artifacts: 'output/*.txt'
        }
    }
}
