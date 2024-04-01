pipeline {
    agent any
    
    stages {
        stage('checkout') {
            steps {
                // Checkout the code from the repository
                git branch: 'master', url: 'https://github.com/sheir296/scd-lab-10.git'
            }
        }
        
        stage('dependency') {
            steps {
                // Install project dependencies
                sh 'npm install'
            }
        }
        
        // You can skip the test stage
        
        stage('build') {
            steps {
                // Build the project
                sh 'npm run build'
            }
        }
        
        stage('Docker Compose Up') {
            steps {
                // Bring up Docker Compose services
                sh 'docker compose up'
            }
        }
    }
}
