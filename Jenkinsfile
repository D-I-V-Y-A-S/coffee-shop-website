pipeline {
    agent any

    stages {
        stage('Deploy') {
            steps {
                echo 'Deploying the HTML file...'
            }
        }
    }

    post {
        always {
            echo 'Pipeline execution finished.'
        }
        success {
            echo 'Pipeline completed successfully!'
        }
        failure {
            echo 'Pipeline failed!'
        }
    }
}
