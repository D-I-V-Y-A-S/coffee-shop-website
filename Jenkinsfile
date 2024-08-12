pipeline {
    agent any

    stages {
        stage('Deploy') {
            steps {
                echo 'Deploying the HTML file...'
            }
        }

        stage('Terraform Init') {
            steps {
                bat 'terraform init'
                echo 'terraform initialized..'
            }
        }

        stage('Terraform Apply') {
            steps {
                bat 'terraform apply -auto-approve'
                echo 'terraform applied..'
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
