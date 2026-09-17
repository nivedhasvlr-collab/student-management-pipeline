pipeline {
    agent any
    parameters {
        choice(name: 'ENVIRONMENT', choices: ['dev', 'staging', 'prod'], description: 'Select the environment')
    }
    stages {
        stage ('Checkout') {
            steps {
                git branch: 'main', url: 'https://github.com/nivedhasvlr-collab/student-management-pipeline'
            }
        }
        stage('Show Parameter') {
            steps {
                echo "Selected environment: ${params.ENVIRONMENT}"
            }
        }
    }
}
