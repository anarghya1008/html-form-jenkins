
pipeline {
    agent any

    environment {
        PATH = "C:\\Windows\\System32;${env.PATH}"
    }

    stages {
        stage('Test HTML Form') {
            steps {
                bat 'python --version'
                bat 'python test_form.py'
            }
        }
    }

    post {
        always {
            echo 'HTML form pipeline execution completed.'
        }
    }
}
