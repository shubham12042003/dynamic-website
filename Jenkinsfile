pipeline {
    agent any

    stages {
        stage('Checkout Code') {
            steps {
                checkout scm
            }
        }

        stage('Deploy to Nginx') {
            steps {
                sh '''
                echo "Deploying website..."
                cp -r * /var/www/website/
                '''
            }
        }

        stage('Restart Nginx') {
            steps {
                sh '''
                sudo systemctl reload nginx
                echo "Deployment completed successfully"
                '''
            }
        }
    }
}
