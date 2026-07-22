pipeline {

    agent any

    stages {
        stage('Checkout') {
            steps {
                echo 'Checking out the code...'
                checkout scm
            }
        }
        stage('Install Dependencies') {
            steps {
                echo 'Installing dependencies...'

                sh 'pip install -r requirements.txt'
            }
        }
        stage('Run Tests') {
            steps {
                echo 'Running tests...'
                sh 'pytest test_app.py'
            }
        }

        stage('Build') {
            steps {
                echo 'Building the application...'
                sh 'python3 app.py'
                // Add build steps here if needed
            }
        }
    }
}