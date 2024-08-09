pipeline {
    agent any

    stages {
       stage('Example') {
            steps {
                echo 'Hello World'
            }
        }
    }

    post {
        success {
            echo 'Completed Successfully!'
        }
        failure {
            echo 'Deployment failed!'
        }
    }
}
