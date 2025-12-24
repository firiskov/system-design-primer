pipeline {
    agent any

    stages {
        stage('Checkout') {
            steps {
                git branch: 'main',
                    url: 'https://github.com/firiskov/system-design-primer.git'
            }
        }

        stage('Run Script') {
            steps {
                sh 'python3 app.py'
            }
        }

        stage('Run Tests') {
            steps {
                sh 'pytest'
            }
        }
    }
}



