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
                sudo cp -r * /var/www/myapp/
                sudo systemctl restart nginx
                '''
            }
        }
    }
}
