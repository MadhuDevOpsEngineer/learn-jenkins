pipeline {
    agent {
        node {
            label 'agent-1'
        }
    }

    stages {
        stage('Build') {
            steps {
                echo 'Building..'
            }
        }
        stage('Test') {
            steps {
                echo 'Testing..'
            }
        }
        stage('Deploy') {
            steps {
                echo 'Deploying....'
            }
        }
    }

    post {
        always {
            echo "i will alwasy echo"
        }
        failure {
            echo "this runs when pipeline is failed"
        }
        success {
            echo "this runs when pipeline is success"
        }
    }
}