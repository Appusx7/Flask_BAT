pipeline {
    agent any

    environment {
        PATH = "C:\\Users\\ALWIN BAIJU\\AppData\\Local\\Programs\\Python\\Python313;C:\\Users\\ALWIN BAIJU\\AppData\\Local\\Programs\\Python\\Python313\\Scripts;${env.PATH}"
    }

    stages {
        stage('Install Dependencies') {
            steps {
                bat 'python -m pip install -r requirements.txt'
            }
        }

        stage('Test') {
            steps {
                bat 'python -m pytest'
            }
        }

        stage('Build') {
            steps {
                bat 'if not exist build mkdir build'
                bat 'copy app.py build\\'
                bat 'copy requirements.txt build\\'
            }
        }
    }
}