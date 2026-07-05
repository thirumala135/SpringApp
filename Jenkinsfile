pipeline {
    agent any

    tools {
        maven 'Maven-3.9.16'
    }

    stages {
        stage('Build') {
            steps {
                bat 'mvn clean compile'
            }
        }

        stage('Test') {
            steps {
                bat 'mvn test'
            }
        }

        stage('Deploy') {
            steps {
                bat 'mvn package'
            }
        }
    }
    post {
          always {
              echo 'Pipeline execution completed.'
          }

          success {
              echo 'Build completed successfully.'
          }

          failure {
              echo 'Build failed.'
          }
      }
}
