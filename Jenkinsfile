pipeline {
    agent any
    
    stages {
        stage('Build') {
            steps {
                echo 'Building or Resolve Dependences!'
                sh 'bundle install'
            }
        }
        stage('Test') {
            steps {
                echo 'Running regression testes'
            }        
        }
        stage('UAT') {
            steps {
                echo 'Wait for User Aceptance'
                input(message: 'Got to production?', ok: 'Yes')
            }
        }
        stage('Prod') {
            steps {
                echo 'WebApp is Ready :)'
            }
        }
    }
}