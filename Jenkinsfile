pipeline{
    agent{
        docker {
            image 'node:6-alpine'
            args '-p 3000:3000'
        }
    }
    stages{
        stage("Build"){
            steps{
                echo "========executing Build========"
                sh 'npm install'
            }
            post{
                always{
                    echo "========always========"
                }
                success{
                    echo "========A executed successfully========"
                }
                failure{
                    echo "========A execution failed========"
                }
            }
        }
    }
}