
pipeline {
    agent any

 
environment {
    PATH = "C:\\Windows\\System32;C:\\Windows;${env.PATH}"
    COMSPEC = "C:\\Windows\\System32\\cmd.exe"
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
