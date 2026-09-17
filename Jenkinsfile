pipeline {
    agent any
    stages {
        stage ('Checkout') {
            steps {
                // Connects to your existing repo
                git branch: 'main', url: 'https://github.com/nivedhasvlr-collab/student-management-pipeline-2'
            }
        }
        stage ('Generate Report') {
            steps {
                // Runs the Python code to make the text file
                bat 'python app.py'
            }
        }
        stage ('Archive Report') {
            steps {
                // Saves the file directly to the Jenkins UI for download
                archiveArtifacts artifacts: 'report.txt', fingerprint: true
            }
        }
    }
}
