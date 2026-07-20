pipeline {
    agent any

    stages {

        stage('Checkout') {
            steps {
                git url: 'https://github.com/snehachopra1611/html_project2.git',
                    branch: 'main'
            }
        }

        stage('Test') {
            steps {
                sh 'test -f index.html'
                echo 'Application file index.html found'
            }
        }

    }

    post {
        success {
            echo 'Pipeline Completed Successfully'
        }

        failure {
            echo 'Pipeline Failed'
        }
    }
}
