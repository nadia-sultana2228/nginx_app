pipeline {
    agent any

    stages {
        stage('Checkout Code') {
            steps {
                git branch: 'main', 'https://github.com/nadia-sultana2228/nginx_app.git'
            }
        }

        stage('Deploy to Nginx') {
            steps {
                sh '''
                sudo cp -r * /var/www/html/
                sudo systemctl restart nginx
                '''
            }
        }
    }
}
