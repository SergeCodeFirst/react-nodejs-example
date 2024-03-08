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
                        echo "Will Shh Later..."
                    }
                    echo "Deployment Complete Successfully..."
                }
            }
        }
    }
}