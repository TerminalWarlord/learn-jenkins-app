pipeline {
    agent any
    stages {
        stage('Build') {
            agent{
                docker{
                    image 'node:18-alpine'
                }
            }
            steps {
                sh '''
                    node --version
                    npm --version
                    ls -la
                    npm ci
                    npm run build
                    ls -la
                '''
            }
        }
    }
}
