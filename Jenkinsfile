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
                    def dockerCmd = 'docker run -p 3080:3080 -d sergevismok/demo-app:1.0'
                    sshagent(['ec2-server-key']) {
                        echo "Deployment Complete 1 Successfully..."
                    }
                    echo "Deployment Complete Successfully..."
                }
            }
        }
    }
}