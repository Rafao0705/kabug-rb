pipeline {
    agent { // utiliza um agente docker que baixa uma imagem do ruby e instala todas dependencias necessarias.
        docker {
            image 'qaninja/rubywd'
        }
    }
    
    stages {
        stage('Build') {
            steps {
                echo 'Building or Resolve Dependencias!'
                sh 'rm -f Gemfile.lock'
                sh 'bundle install'
            }
        }
        stage ('Test') {
            steps {
                echo 'Running regression tests'
                sh 'cucumber -p ci'
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