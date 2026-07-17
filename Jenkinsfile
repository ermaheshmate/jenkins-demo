pipeline {

    agent any

    stages {

        stage('Clone Information') {
            steps {
                echo "Starting Jenkins Pipeline"
            }
        }

        stage('Show Files') {
            steps {
                sh 'pwd'
                sh 'ls -la'
            }
        }

        stage('Read File') {
            steps {
                sh 'cat index.txt'
            }
        }

        stage('Build') {
            steps {
                sh './build.sh'
            }
        }

        stage('Git History') {
            steps {
                sh 'git log --oneline'
            }
        }

    }

    post {

        success {
            echo "Build Successful"
        }

        failure {
            echo "Build Failed"
        }

        always {
            echo "Pipeline Finished"
        }

    }
}
