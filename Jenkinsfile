pipeline {
    agent any

    stages {
        stage('Deploy Website') {
            steps {
                sh '''
                echo "Deploying website..."
                cp index.html /var/www/website/
                sudo systemctl reload nginx
                echo "Deployment completed"
                '''
            }
        }
    }
}
