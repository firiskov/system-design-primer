pipeline {
    agent {
        docker {
            image 'python:3.11-slim'
        }
    }
    
    stages {
        stage('Install Dependencies') {
            steps {
                sh '''
                    python --version
                    pip install pytest
                '''
            }
        }
        
        stage('Run Application') {
            steps {
                sh 'python app.py'
            }
        }
        
        stage('Run Tests') {
            steps {
                sh 'pytest test_app.py -v'
            }
        }
    }
    
    post {
        always {
            echo 'Pipeline завершен'
        }
        success {
            echo 'Все этапы выполнены успешно!'
        }
        failure {
            echo 'Пайплайн завершился с ошибкой'
        }
    }
}
