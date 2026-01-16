pipeline {
    agent any

    environment {
        PATH = "/home/jenkins/.local/bin:/usr/bin:/bin"
    }

    stages {
        stage('Install Dependencies') {
            steps {
                sh 'python3 -m pip install --user -r requirements.txt'
            }
        }

        stage('Start Flask App') {
            steps {
                sh '''
                pkill -f app.py || true
                nohup python3 app.py > app.log 2>&1 &
                sleep 10
                '''
            }
        }
    }
}
