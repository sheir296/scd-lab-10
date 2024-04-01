pipeline {
    agent any
    
    stages {
        stage('checkout') {
            steps {
                sh 'git pull https://github.com/sheir296/scd-lab-10.git'
            }
        }
        
        stage('dependency') {
            steps {
                sh 'npm install'
            }
        }
        
        stage('build') {
            steps {
                sh 'cd jenkins/app/models'
            }
        }
        
        stage('test') {
            steps {
                sh 'npm test'
            }
        }
        
        stage('Docker Comopse Up') {
            steps {
                sh "docker compose up"
            }
        }
    }
}
