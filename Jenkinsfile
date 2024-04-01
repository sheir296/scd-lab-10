pipeline {

    agent any

    stages {
         stage('build') {
          steps {
              bat 'npm install'
            }
          }

        stage('Docker Comopse Up') {
            steps {

                    bat "docker compose up"

            }
        }
         stage('kill') {
            steps {

                    bat "docker compose down"

            }
        }
    }
}
