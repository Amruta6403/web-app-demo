pipeline {
  agent any
  environment { DEPLOY_DIR = 'C:\\inetpub\\wwwroot' }
  stages {
    stage('Checkout') { steps { git branch: 'main', url: 'https://github.com/yourusername/web-app-demo.git' } }
    stage('Build') { steps { bat 'echo Build: listing && dir' } }
    stage('Test') { steps { bat 'where tidy || echo tidy not found' } }
    stage('Deploy') { steps { bat 'mkdir deployed 2>nul || exit 0 & xcopy /Y index.html deployed\\' } }
  }
}

