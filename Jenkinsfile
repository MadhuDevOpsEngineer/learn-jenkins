pipeline {
    agent {
        node {
            label 'agent-1'
        }
    }
        environment {


            GREETINGS = "Hello Jenkins"
        }

    stages {
        stage('Build') {
            steps {
                echo 'Building..'
            }
        }
        stage('Test') {
            steps {
                echo 'Testing..webhook'
            }
        }
        stage('Deploy') {
            steps {
                sh """
                 echo "here i wrote shellscript"
                 echo "$GREETINGS"

                """
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