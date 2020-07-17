pipeline {
    agent any
    
    stages {
        stage('Build') {
            steps {
                echo 'Building or Resolve Dependencias!'
                sh 'bundle install'
            }
        }
        stage ('Test') {
            steps {
                echo 'Running regression tests'
            }
        }
        stage ('UAT') {
            steps {
                echo 'Wait for User Acceptance'
                input(message: 'Got to production?', ok: 'Yes')
            }
        }
        stage ('Prod') {
            steps {
                echo 'WebApp is Ready!'
            }
        }
    }
}