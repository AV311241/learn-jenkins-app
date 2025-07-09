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
                echo "hello jenkins "
                echo "i am abhishek"
                echo "i am abhishek"

            }
        } 
    }
}
