pipeline {
    agent any
    
    stages {
        stage('Setup Python') {
            steps {
                sh '''
                    python3 --version
                    pip3 --version
                    pip3 install pytest
                '''
            }
        }
        
        stage('Run Application') {
            steps {
                sh 'python3 app.py'
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
