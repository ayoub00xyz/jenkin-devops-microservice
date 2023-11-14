pipeline {
    agent any

    stages {
        stage('Build') {
            agent {
                docker { 
                    image 'maven:3.6.3' 
                }
            }
            steps {
                echo "Build"
                sh "mvn --version"
            }
        }
        stage('Test') {
            steps {
                echo "Test"
            }
        }
        stage('Integration Test') {
            agent {
                docker { 
                    image 'maven:3.6.3' 
                }
            }
            steps {
                echo "Integration Test yaaay"
            }
        }
    }

    post {
        always {
            echo "I'm awesome. I always run"
        }
        success {
            echo "I run when you are successful"
        }
        failure {
            echo "I run when you fail"
        }
    }
}
