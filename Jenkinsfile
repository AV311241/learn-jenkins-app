pipeline {
    agent any
    stages {
        stage("Build React App") {
            agent {
                docker {
                    image 'node:18'  // 🟢 use full image, not alpine
                    reuseNode true
                }
            }
            steps {
                sh '''
                    echo "Node Version:"
                    node -v

                    echo "NPM Version:"
                    npm -v

                    echo "Cleaning cache and previous installs"
                    npm cache clean --force
                    rm -rf node_modules package-lock.json

                    echo "Installing dependencies"
                    npm install

                    echo "Running build"
                    npm run build
                '''
            }
        }
    }
}
