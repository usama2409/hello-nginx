pipeline {
    agent any

    stages {
        stage('Checkout') {
            steps {
                git branch: 'main',
                    url: 'https://github.com/usama2409/hello-nginx.git'
            }
        }

        stage('Deploy to NGINX') {
            steps {
                sh '''
                sudo cp index.html /usr/share/nginx/html/index.html
                sudo systemctl reload nginx
                '''
            }
        }
    }
}
