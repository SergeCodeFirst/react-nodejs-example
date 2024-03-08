pipeline {
    agent any
    stages {
        stage("test") {
            steps {
                script {
                    echo "Testing the application..."
                }
            }
        }

        stage("build") {
            steps {
                script {
                    echo "Building the application..."
                }
            }
        }
        
        stage("deploy") {
            steps{
                script {
                    echo "Start Deploying the application..."
                    sshagent(['ec2-server-key']) {
                        def dockerCmd = 'docker run -p 3080:3080 -d sergevismok/demo-app:1.0'
                        sh "ssh -o StrictHostKeyChecking=no ec2-user@54.90.134.212 ${dockerCmd}"
                    }
                    echo "Deployment Complete Successfully..."
                }
            }
        }
    }
}