  GNU nano 8.4                    Jenkinsfile                             
pipeline {
    agent any

    stages {
        stage('Checkout') {
            steps {
                git 'https://github.com/donnemartin/system-design-primer.>
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



