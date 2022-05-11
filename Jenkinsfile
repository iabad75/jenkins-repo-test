pipeline {
    agent {
        docker { image 'node:16.13.1-alpine' }
    }
    
    stages {
        stage('Test') {
            steps {
                sh 'node --version'
            }
        }
    }
    
    post {
        always {
            emailext body: 'Test Message', subject: 'Test Subject', to: 'masalinas.gancedo@gmail.com'
        }
    }    
}
