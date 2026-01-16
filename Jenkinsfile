pipeline {
    agent any

    stages {
        stage('Checkout Code') {
            steps {
                echo 'Code checked out from GitHub'
            }
        }

        stage('Run Python App') {
            steps {
                sh 'python3 app.py'
            }
        }
    }
}
