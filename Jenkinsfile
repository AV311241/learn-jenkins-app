pipeline {
    agent any
    stages{
        stage("build"){
            agent {
                docker {
                    image 'node:18-alpine'
                    reuseNode true
                }
            }
            steps{
                cleanWs()
                sh '''
                    node --version
                    npm --version
                    npm install
                    npm run build
                
                '''
            }
        } 
    }
}
