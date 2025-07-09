pipeline {
    agent any
    stages{
        stage("build"){
            agent {
                docker {
                    image 'node:24-alpine'
                    reuseNode true
                }
            }
            steps{
                sh '''
                    node --version
                    npm --version
                    npm ci
                    npm run build
                
                '''
            }
        } 
    }
}
