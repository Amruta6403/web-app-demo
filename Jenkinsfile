
pipeline {
    agent any
    stages {
        stage('Checkout') {
            steps {
                git branch: 'main', url: 'https://github.com/yourusername/web-app-demo.git'
            }
        }
        stage('Build') {
            steps {
                echo 'Build Step: Checking files'
            }
        }
        stage('Test') {
            steps {
                echo 'Test Step: Validate HTML (optional)'
            }
        }
        stage('Deploy') {
            steps {
                echo 'Deploy Step: Copy files to web server'
                // Windows: bat "xcopy /Y index.html C:\\inetpub\\wwwroot\\"
                // Linux: sh "cp index.html /var/www/html/"
            }
        }
    }
}
