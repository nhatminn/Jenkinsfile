pipeline {
    agent any

    environment {
        DIRECTORY_PATH = "/var/lib/codebase"          // change if needed
        TESTING_ENVIRONMENT = "staging-server"
        PRODUCTION_ENVIRONMENT = "MinhTran"           // your name as prod env
    }

    stages {
        stage('Build') {
            steps {
                echo "Fetch the source code from the directory path specified by the environment variable"
                echo "DIRECTORY_PATH value: ${env.DIRECTORY_PATH}"
                echo "Compile the code and generate any necessary artefacts"
            }
        }

        stage('Test') {
            steps {
                echo "Unit tests"
                echo "Integration tests"
            }
        }

        stage('Code Quality Check') {
            steps {
                echo "Check the quality of the code"
            }
        }

        stage('Deploy') {
            steps {
                echo "Deploy the application to a testing environment specified by the environment variable"
                echo "Testing environment: ${env.TESTING_ENVIRONMENT}"
            }
        }

        stage('Approval') {
            steps {
                echo "Waiting 10 seconds to simulate manual approval..."
                sleep 10
            }
        }

        stage('Deploy to Production') {
            steps {
                echo "Deploying the application to the production environment: ${env.PRODUCTION_ENVIRONMENT}"
            }
        }
    }
}
