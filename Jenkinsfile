pipeline {
    agent any

    stages {
        stage('Install Dependencies') {
            steps {
                sh 'sudo python3 -m pip install -r requirements.txt'
            }
        }

        stage('Restart Flask App') {
            steps {
                sh 'sudo systemctl restart flask-app'
            }
        }
    }
}
