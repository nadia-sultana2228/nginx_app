pipeline {
    agent any
    stages {
        stage('Checkout Code') {
            steps {
                git branch: 'main', url: 'https://github.com/nadia-sultana2228/nginx_app.git'
            }
        }
        stage('Deploy to Nginx') {
            steps {
                sh '''
                sudo cp -r Jenkinsfile README.md index.html style.css /var/www/html/
                '''
            }
        }
    }
}
