pipeline {
    agent any

    stages {
        stage('Checkout') {
            steps {
                git branch: 'main',
                    url: 'https://github.com/usama2409/hello-nginx.git'
            }
        }

        stage('Deploy to Apache') {
            steps {
                sh '''
                sudo cp index.html /var/www/html/index.html
                sudo systemctl reload httpd
                '''
            }
        }
    }
}
