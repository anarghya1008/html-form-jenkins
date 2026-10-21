
pipeline {
    agent any

    stages {
        stage('Checkout') {
            steps {
                git branch: 'main',
                    url: 'https://github.com/anarghya1008/html-form-jenkins.git'
            }
        }

        stage('Test HTML Form') {
            steps {
                script {
                    if (isUnix()) {
                        sh 'python3 test_form.py'
                    } else {
                        bat 'python test_form.py'
                    }
                }
            }
        }
    }

    post {
        always {
            echo 'HTML form pipeline execution completed.'
        }
    }
}
